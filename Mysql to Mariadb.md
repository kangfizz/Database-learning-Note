## Target : Move your origin database mysql to mariadb
####前言:因為mariadb相較於mysql更加多容量 加上mysql被oracle買下後，其實狀況不佳，藉此寫一篇文章告知如何轉換。

###Step1:  
sudo apt-get remove --purge mysql-server mysql-client mysql-common  
sudo apt-get autoremove  
sudo apt-get autoclean  
sudo apt-get install mariadb-server  
  
以上四行打入終端機 在第一行輸入後會問你是否要清空在mysql裡的資料，如果要保留請選擇”No”  
  
進入mariadb:   mysql –u root -p  
  
###Step2:  
對於odbcconnector的錯誤；  
apt-get install r-cran-rodbc unixodbc unixodbc-bin odbcinst libmyodbc mariadb-client r-cran-rmysql  
  
(以上重載connector)  
  
###額外介紹:  
這些設定要在/etc/odbc.ini調整  
  
之後請參考node.js學習筆記 有關myphpadmin安裝  
