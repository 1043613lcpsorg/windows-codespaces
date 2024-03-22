how to Install windows in github codespaces 
1. make a blank codespace ![Screenshot 2024-03-22 8 04 10 AM](https://github.com/1043613lcpsorg/windows-codespaces/assets/153699099/79e75d5a-a2d8-42df-a865-e4db181e275d)
2. type in terminal `ls -a` then type `clear`
3. type in terminal `sudo apt update`
4. then type in `sudo apt install qemu-kvm qemu-system-x86 openbox firefox tigervnc-standalone-server` when it asks to download 950 mb type y
5. after that then git clone `git clone https://www.github.com/novnc/noVNC`
6. type `cd noVNC`
7. and `ls`
8. then type `sudo vncserver -SecurityType none -xstartup "openbox" -rfbport 5900`
9. now you are half way through
10. don't click "open in browser" close the popup
11. then in terminal type in `sudo ./utils/novnc_proxy --vnc 127.0.0.1:5900 --listen localhost:6080`
12. now click the popup that says open in browser 
in the webpage click vnc.html
then press connect if the screen is black then you might be already connected when you open the html file
left click then click open browser
search up `Windows 11`
click the link that says windows 11
![Screenshot 2024-03-22 8 30 38 AM](https://github.com/1043613lcpsorg/windows-codespaces/assets/153699099/676c912b-3ea5-405d-8271-5bbc197a986b)
1. download windows 11 (DOWNLOAD THE ISO NOT THE EXECUTABLE) in the vm
2. the download goes very fast in the vm it took me 30 seconds
3. while the windows 11 iso is downloading go back to the codespace and make a new terminal 
![Screenshot 2024-03-22 8 34 57 AM](https://github.com/1043613lcpsorg/windows-codespaces/assets/153699099/2ff07b91-e79c-4bb8-89f9-bf5c834d07c2)
4. type `sudo apt install konsole`
5. when asking "do you want to download 350 mb?" type `y`
6. watch this but it runs in 2 times speed https://www.youtube.com/watch?v=PQv-1-qI9zg
7. once konsole has downloaded close firefox and leftclick and open the emulator terminal
8. type `ls`
9. then type `cd Downloads` make sure the "D" for the Dowloads is capitalized
10. then type `df -h` after that type `qemu-img create disk.img 10G`
11. in the emulator terminal first type `cd Downloads` then type `ls` copy the windows iso name then type `qemu-system-x86-64 --enable-kvm -m 4G -smp 2 -pflash /usr/share/OVMF/OVMF_CODE.fd -hdd disk.img - cdrom drive Win11_22H2_English_x64v2.iso`
