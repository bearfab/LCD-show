
###라즈베리파이 3.5인치 디스플레이 드라이버 설치 방법  
====================================================

1.)라즈베리파이 OS를 설치
====================================================
  a)라즈베리파이 OS 다운로드 페이지 접속후 이미지 다운로드<br>
  https://www.raspberrypi.org/downloads/<br>
  b) 라즈베리파이 이미지 라이팅용 프로그램(이미저, Etcher 등) 다운로드
  c) 이미지 라이팅용 프로그램을 사용해서 SD카드나 USB에 이미지를 라이팅합니다.
       
2.) ssh를 통해 라즈베리파이에 접속 <br>
====================================================
  a) sd카드를 컴퓨터에 꽂고  sd카드의 boot파티션에 ssh이라는 이름의 파일 생성
  b) 라즈베리파이에 랜선, sd카드를 꽂고 부팅 후
  c) 데스크탑에서 putty등의 프로그램을 사용해서 라즈베리파이에 ssh로 접속
     
2.) 드라이버 저장소 클론<br>
====================================================
```git clone https://github.com/goodtft/LCD-show.git```<br>
```chmod -R 755 LCD-show```<br>
```cd LCD-show/```<br>
  
3.)Step3, According to your LCD's type, excute the corresponding driver:
====================================================

# 2.4” RPi Display (MPI2401):
### Driver install:
sudo ./LCD24-show
### WIKI:
CN: http://www.lcdwiki.com/zh/2.4inch_RPi_Display  <br>
EN: http://www.lcdwiki.com/2.4inch_RPi_Display
 

# 2.4” RPi Display For RPi 3A+ (MPI2411):
### Driver install:
sudo ./LCD24-3A+-show  
### WIKI:
CN: http://www.lcdwiki.com/zh/2.4inch_RPi_Display_For_RPi_3A+   <br>
EN: http://www.lcdwiki.com/2.4inch_RPi_Display_For_RPi_3A+

# 2.8” RPi Display (MPI2801):
### Driver install:
sudo ./LCD28-show 
### WIKI:
CN: http://www.lcdwiki.com/zh/2.8inch_RPi_Display  <br>
EN: http://www.lcdwiki.com/2.8inch_RPi_Display
  
# 3.2” RPi Display (MPI3201):
### Driver install:
sudo ./LCD32-show   
### WIKI:
CN: http://www.lcdwiki.com/zh/3.2inch_RPi_Display  <br>
EN: http://www.lcdwiki.com/3.2inch_RPi_Display

# MHS-3.2” RPi Display (MHS3232):
### Driver install:
sudo ./MHS32-show   
### WIKI:
CN: http://www.lcdwiki.com/zh/MHS-3.2inch_Display  <br>
EN: http://www.lcdwiki.com/MHS-3.2inch_Display

# 3.5” RPi Display(MPI3501):
### Driver install:
sudo ./LCD35-show
### WIKI:
CN: http://www.lcdwiki.com/zh/3.5inch_RPi_Display  <br>
EN: http://www.lcdwiki.com/3.5inch_RPi_Display
   
# 3.5” HDMI Display-B(MPI3508):
### Driver install:
sudo ./MPI3508-show
### WIKI:
CN: http://www.lcdwiki.com/zh/3.5inch_HDMI_Display-B  <br>
EN: http://www.lcdwiki.com/3.5inch_HDMI_Display-B
    
# MHS-3.5” RPi Display(MHS3528):
### Driver install:
sudo ./MHS35-show
### WIKI:
CN: http://www.lcdwiki.com/zh/MHS-3.5inch_RPi_Display  <br>
EN:http://www.lcdwiki.com/MHS-3.5inch_RPi_Display

# MHS-3.5” RPi Display-B(MHS35XX):
### Driver install:
sudo ./MHS35B-show
### WIKI:
CN: http://www.lcdwiki.com/zh/MHS-3.5inch_RPi_Display-B  <br>
EN:http://www.lcdwiki.com/MHS-3.5inch_RPi_Display-B

# 4.0" HDMI Display(MPI4008):
### Driver install:
sudo ./MPI4008-show
### WIKI:
CN: http://www.lcdwiki.com/zh/4inch_HDMI_Display-C  <br>
EN: http://www.lcdwiki.com/4inch_HDMI_Display-C
   
# MHS-4.0" HDMI Display-B(MHS4001):
### Driver install:
sudo ./MHS40-show
### WIKI:
CN: http://www.lcdwiki.com/zh/MHS-4.0inch_Display-B  <br>
EN: http://www.lcdwiki.com/MHS-4.0inch_Display-B
  
# 5.0” HDMI Display(Resistance touch)(MPI5008):
### Driver install:
sudo ./LCD5-show
### WIKI:
CN: http://www.lcdwiki.com/zh/5inch_HDMI_Display  <br>
EN: http://www.lcdwiki.com/5inch_HDMI_Display
    
# 5inch HDMI Display-B(Capacitor touch)(MPI5001):
### Driver install:
sudo ./MPI5001-show
### WIKI:
CN: http://www.lcdwiki.com/zh/5inch_HDMI_Display-B  <br>
EN: http://www.lcdwiki.com/5inch_HDMI_Display-B
    
# 7inch HDMI Display-B-800X480(MPI7001):
### Driver install:
sudo ./LCD7B-show
### WIKI:
CN: http://www.lcdwiki.com/zh/7inch_HDMI_Display-B  <br>
EN: http://www.lcdwiki.com/7inch_HDMI_Display-B
   
# 7inch HDMI Display-C-1024X600(MPI7002):
### Driver install:
sudo ./LCD7C-show
### WIKI:
CN: http://www.lcdwiki.com/zh/7inch_HDMI_Display-C  <br>
EN: http://www.lcdwiki.com/7inch_HDMI_Display-C
   
Wait for a moment after executing the above command, then you can use the corresponding raspberry LCD.




# How to rotate the display direction

This method only applies to the Raspberry Pi series of display screens, other display screens do not apply.

### Method 1, If the driver is not installed, execute the following command (Raspberry Pi needs to connected to the Internet):

sudo rm -rf LCD-show<br>
git clone https://github.com/goodtft/LCD-show.git<br>
chmod -R 755 LCD-show<br>
cd LCD-show/<br>
sudo ./XXX-show 90<br>

After execution, the driver will be installed. The system will automatically restart, and the display screen will rotate 90 degrees to display and touch normally.<br>
( ' XXX-show ' can be changed to the corresponding driver, and ' 90 ' can be changed to 0, 90, 180 and 270, respectively representing rotation angles of 0 degrees, 90 degrees, 180 degrees, 270 degrees)<br>

### Method 2, If the driver is already installed, execute the following command:

cd LCD-show/<br>
sudo ./rotate.sh 90<br>

After execution, the system will automatically restart, and the display screen will rotate 90 degrees to display and touch normally.<br>
( ' 90 ' can be changed to 0, 90, 180 and 270, respectively representing rotation angles of 0 degrees, 90 degrees, 180 degrees, 270 degrees)<br>
(If the rotate.sh prompt cannot be found, use Method 1 to install the latest drivers)



