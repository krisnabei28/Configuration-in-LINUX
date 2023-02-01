# Setting <b>SQL DEVELOPER</b> di LINUX

- Download **Sql Developer** : https://www.oracle.com/database/sqldeveloper/technologies/download/
- Pilih opsi **Other Platforms**, lalu download **sqldeveloper-<i>number</i>-no-jre.zip**
- Setelah selesai di download, buka command linux dan lakukan unzip pada file yang di download tadi. Command : <i>unzip sqldeveloper-number-no-jre.zip</i>
- Setelah file selesai di unzip, lakukan beberapa command line berikut :
    -     sudo mv sqldeveloper /opt
    -     cd /opt/sqldeveloper/
    -     nano sqldeveloper.sh
    -     Copy script berikut kedalam sqldeveloper.sh :
           #!/bin/bash
           #cd "`dirname $0`"/sqldeveloper/bin && bash sqldeveloper $*
           unset -v GNOME_DESKTOP_SESSION_ID

           cd /opt/sqldeveloper/sqldeveloper/bin && bash sql developer $*
    -     sudo chmod +x sqldeveloper.sh
    -     ./sqldeveloper.sh (run sql developer)  
- Script untuk **SQL DEVELOPER DESKTOP**
    -     sudo ln -s /opt/sqldeveloper/sqldeveloper.sh /usr/local/bin/sqldeveloper
    -     cd /usr/share/applications
    -     sudo nano sqldeveloper.desktop
    -     [Desktop Entry]
          Exec=sqldeveloper
            Terminal=false
            StartupNotify=true
            Categories=GNOME;Oracle;
            Type=Application
            Icon=/opt/sqldeveloper/icon.png
          Name=Oracle Sql Developer
    -     cd
    -     sqldeveloper (run sql developer) 
- **SQL DEVELOPER** berhasil diinstal