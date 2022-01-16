# cyber-security-projects

This project contains simple cyber security projects which are as follows:


# keylogger

Keyloggers are programs that capture your key strokes.
They can be used to keep logs of everything you press on the keyboard but on the 
flip side it can be used for malicious purposes as well.

The keylogger that I've made is a basic keylogger with not much functionality as the ones available in market today.
It captures your keystrokes and saves them in a file "keylogger.txt".
It then sends the contents of the file(i.e. the keystrokes) to your email id.

With some extra lines of code, it can also send the keystrokes at regular intervals.
But that is a project for another time.
SYNTAX : python keylogger.py

[NOTE: You need to press esc key to exit out the keylogger.]

You need to have pynput , smtplib and ssl installed.

While python comes with the library smtplib and ssl preinstalled.
You can install pynput with :
pip install pynput


# Virus total 

<h5>This script lets one identify whether the suspicious file is a malware or not</h5>
<b>Syntax:</b><em>./virus_total.py &lt;file_name&gt;</em>
<h4>Or</h4>
<b>Syntax:</b><em>python virus_total.py &lt;file_name&gt;</em>

# LSB Steganography

This Project Describes the use of LSB Steganography.<br>
Do check the python script written to implement lsb steganography<br>
<p style="color: grey" >#./stego -f &lt;filename.png&gt; -e &lt;secret_message&gt; -p &lt;Password (Optional) &gt; : To embed a secret message. <br>
#./stego -f &lt; secretfile.png &gt; -x -p &lt; Password supplied &gt; : To extract the secret message.<br>
#Note : Even if you passed a blank field in the -p argument,while creating a secret file, you must append a -p while extracting the message. </P>

STEGANOGRAPHY  comes  from  the  Greek  Words:  STEGANOS  –  “Covered”,  GRAPHIE  –  “Writing”.
The sender hides his/her message within an image/audio/video.Since the algorithm uses the lease significant bit to hide the secret message the change is undectable by a naked eye.<br>
The various types of steganography include:
<br>
<ul>
  <li>Image Steganography</li>
  <li>Audio  Steganography</li>
  <li>Video Steganography</li>
  <li>Text files Steganography</li>
  </ul>
<br>
Types of Images:
<ul>
  <li>Black and white</li>
  <li>Geryscale</li>
  <li>RGB</li>
</ul>
<p>In a gray scale image each pixel is represented in 8 bits. The last bit in a pixel is called as Least Significant bit as its value will affect the pixel value only by “1”. So, this property is used to hide the data in the image. If anyone have considered last two bits as LSB bits as they will affect the pixel value only by “3”</P>
<p>  The  LSB  embedding  approach  has become the basis of many techniques that hide messages within multimedia carrier data. LSB embedding may even be  applied  in  particular  data  domains  –  for  example,  embedding  a  hidden  message  into  the  color  values  of  RGB bitmap data</p>

<h3>Let's study the application of LSB on a Greyscale Image</h3>
<p>In a Greyscale image, each pixel is represented by 8 bits, while in a RGB it is 24 bits</p>
<p>Suppose the following are some of the bits in a Grayscale image</p>
<p>11110011 <br> 11011011 <br>10110110 <br> 11011100<br>11011111 <br> 11010111 <br> 00100110 <br> 01000011</p>
<h4>You wish to hide "A" in it. The ascii value of "A" is 10000001.</h4>
<p>The algorithm simply replaces the last bit of the bytes with the consecutive bits of the letter "A", Giving us </p>
<p>11110011 <br> 11011010 <br>10110110 <br> 11011100<br>11011110 <br> 11010110 <br> 00100110 <br> 01000011</p>

<h2>Steganalysis</h2>
<p>Steganalysis is the study of detecting messages hidden using steganography</p>
<p>LSB Steganography can be detected by looking at the histograms of the files</p>
<p>Also lossy compression technique can render LSB Steganography useless to an extent, so lossless compression techniques should be used</p>


# ServerSideTemplateInjection
I've tried to emulate Server Side Template Injection using flask web-framework.
<h1>Server-Side Template Injection </h1> <br>
Server-side template injections (SSTI) are vulnerabilities that let the attacker inject code into such server-side templates. In simple terms, the attacker can introduce code that is actually processed by the server-side template. This may result in remote code execution (RCE)
<hr>
<h2>Steps</h2>
<p>pip3 install Flask</p>
<p>pip3 install virtualenv</p>
<h5>On Linux </h5>

<ul>
  <li>mkdir SSTIProject </li>
  <li>cd SSTIProject </li>
  <li>python3 -m venv venv</li>
 </ul>
 
<h5>On Windows </h5>

<ul>
  <li>mkdir SSTIProject </li>
  <li>cd SSTIProject </li>
  <li>p3 -m venv venv</li>
 </ul>
 
<p><b>Windows:</b> set FLASK_APP=hello.py</p>
<p><b>Linux:</b> export FLASK_APP=hello.py</p>
<p>All you have to do now is run</p>
<p>flask run</p> 


# Scanner
These are basic scanners.

They can check the number of devices connected to your network and print their local IP addresses along with their MAC addresses.

1. Sniff_Tool.py
_________________

I have used argparse and scapy to make this basic network scanner.

[Syntax : python &lt;file_name&gt; -ip &lt;ip_address&gt;/&lt;subnet&gt;]

[NOTE : Use it with root/administrative priviledges]

One needs to have argparse and scapy installed.

They can be installed with :

   pip install argparse

   pip install scapy
   
   
   
   OUTPUT : 
   
   {'ip': '192.168.1.1', ' mac': '7c:a9:6b:07:6e:14'}
   
   {'ip': '192.168.1.3', ' mac': '88:11:96:ff:79:a0'}
   
   {'ip': '192.168.1.10', ' mac': '68:db:f5:84:80:7f'}
   
   {'ip': '192.168.1.4', ' mac': 'd4:f5:47:17:b0:a6'}
   
   {'ip': '192.168.1.14', ' mac': 'a4:c3:f0:4f:a5:06'}
   
   {'ip': '192.168.1.2', ' mac': '6c:56:97:b0:fe:b3'}
   
   {'ip': '192.168.1.26', ' mac': '28:6c:07:8c:96:f5'}

   

2. Sniff_Tool2.py
__________________

I have used sys and scapy to build this basic network scanner.

Call it from the command line using root/admin privileges

[Syntax : python &lt;file_name&gt; &lt;ip_address&gt;/&lt;subnet&gt;]

[Note : Put the ip address of your default gateway(router) to get all the client's ip address.]
Scapy can be installed with : 
  
   pip install scapy



# phishing
FOR Phishing(Without PHP)
__________________________
Phishing is an attempt to display onself as an authentic source in order to steal the credentials of the victim.

Phising attacks are common and it is not possible to distinguish the original site from the disguised one.

The only way you have is by looking at the URL.

I have Used Node.js, with express as a framework.
This code runs locally on your machine on port 3000.

It creates a file called logs.json that stores all the credentials of the users who attempt to register.

If you wish to replicate this, you need to have node.js installed.

You need to install express,ejs and body-parser as well.

Node.js can be downloaded from thier official site https://nodejs.org/en/download/

To install express, ejs and body-parser :npm install express,ejs,body-parser

FOR Phishing(Using PHP)
________________________
This can be hosted on a platform such as https://in.000webhost.com/ for free.

Unlike the former one, this can have serious consequenses as this will be available online.So, don't use it for your advantage.

Like the previous one, I have customized the login page, but one can add the contents as per one's choice.

One has to just right click on the page and click on "View Page source" and copy the source code to phishing.html

NOTE: One has to change the "action" attribute to "login_details.php".




