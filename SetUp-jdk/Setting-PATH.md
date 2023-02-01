# Setting <b>JDK</b> di LINUX

- Download `JDK` : https://www.oracle.com/java/technologies/downloads/#java11
- Pilih dam download `x64 Debian Package` pada bagian menu LINUX
- Setelah berhasil di download, silahkan membuka command pada LINUX
- Masukkan command line berikut: 
    -     sudo dpkg -i jdk-package.deb
    -     sudo update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk-11.0.9/bin/java 1 
          (Sesuaikan dengan jdk yang digunakan, contohnya jdk-11.0.9)
    -     java --version
    -     sudo update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/jdk-11.0.9/bin/javac 1
    -     javac --version
    -     sudo update-alternatives --config java
    -     sudo gedit /etc/environment
    -     Di dalam enviroment, masukkan JAVA_HOME="/usr/lib/jvm/jdk-11.0.9"
          (Sesuaikan dengan jdk yang digunakan)
    -     source /etc/environment
    -     echo $JAVA_HOME
- `JDK` berhasil diinstall
