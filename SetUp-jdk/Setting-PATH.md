# Setting <b>JDK</b> di LINUX

- Download **JDK** : https://www.oracle.com/java/technologies/downloads/#java11
- Pilih dam download **x64 Debian Package** pada bagian menu LINUX
- Setelah berhasil di download, silahkan membuka command pada LINUX
- Masukkan command line berikut: 
    - <i>sudo dpkg -i jdk-package.deb</i>
    - <i>sudo update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk-11.0.9/bin/java 1</i> (Sesuaikan dengan jdk yang digunakan, contohnya jdk-11.0.9)
    - <i>java --version</i>
    - <i>sudo update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/jdk-11.0.9/bin/javac 1</i>
    - <i>javac --version</i>
    - <i>sudo update-alternatives --config java</i>
    - <i>sudo gedit /etc/environment</i>
    - Di dalam enviroment, masukkan <i>JAVA_HOME="/usr/lib/jvm/jdk-11.0.9"</i> (sesuaikan dengan jdk yang digunakan)
    - <i>source /etc/environment</i>
    - <i>echo $JAVA_HOME</i>
- **JDK** berhasil diinstall
