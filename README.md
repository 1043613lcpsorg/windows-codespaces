how to Install windows in github codespaces 
1. make a blank codespace ![Screenshot 2024-03-22 8 04 10 AM](https://github.com/1043613lcpsorg/windows-codespaces/assets/153699099/79e75d5a-a2d8-42df-a865-e4db181e275d)
2. type in terminal `ls -a` then type `clear`
3. type in terminal `sudo apt update`
4. then type in `sudo apt install qemu-kvm qemu-system-x86 openbox firefox tigervnc-standalone-server`
5. after that then git clone `git clone https://www.github.com/novnc/noVNC`
6. type `cd noVNC`
7. and `ls`
8. then type `sudo vncserver -SecurityType none -xstartup "openbox" -rfbport 5900`
9. now you are half way through
10. don't click "open in browser" close the popup
11. then in terminal type in `sudo ./utils/novnc_proxy --vnc 127.0.0.1:5900 --listen localhost:6080`
12. now click the popup that says open in browser 
