# Setting <b>SQL DATAMODELER</b> di LINUX

- Download `SQL DATAMODELER` : https://www.oracle.com/database/sqldeveloper/technologies/sql-data-modeler/download/
- Pilih opsi `Windows 32-bit/64-bit`, lalu download `datamodeler-22.2.0.165.1149-no-jre.zip`
- Opsi `Windows 32-bit/64-bit` dipilih dengan tujuan hanya akan mengambil `datamodeler.sh`
- Setelah selesai di download, buka command linux dan lakukan unzip pada file yang di download tadi. Command : `unzip datamodeler-22.2.0.165.1149-no-jre.zip`
- Setelah file selesai di unzip, lakukan beberapa command line berikut :
    -     sudo mv datamodeler /opt
    -     cd /opt/datamodeler/
    -     nano datamodeler.sh
    -     Copy script berikut kedalam sqldeveloper.sh :
           #!/bin/bash
           #cd "`dirname $0`"/datamodeler/bin && bash datamodeler $*
           unset -v GNOME_DESKTOP_SESSION_ID

           cd /opt/datamodeler/datamodeler/bin && bash datamodeler $*
    -     sudo chmod +x datamodeler.sh
    -     ./datamodeler.sh (run datamodeler)  
- Script untuk `SQL DATAMODELER DESKTOP`
    -     sudo ln -s /opt/datamodeler/datamodeler.sh /usr/local/bin/datamodeler
    -     cd /usr/share/applications
    -     sudo nano datamodeler.desktop
    -     [Desktop Entry]
          Exec=datamodeler
            Terminal=false
            StartupNotify=true
            Categories=GNOME;Oracle;
            Type=Application
            Icon=/opt/datamodeler/icon.png
          Name=Oracle Sql Datamodeler
    -     cd
    -     Sql Datamodeler (run Sql Datamodeler) 
- `SQL DATAMODELER` berhasil diinstal