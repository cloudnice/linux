# Linux Kullanıcı Yönetimi ve Geçiş Komutları 

# Kullanıcı Oluşturma
sudo adduser <kullanıcı_adı>
# Örneğin: sudo adduser ahmet

# Kullanıcının Gruba Eklenmesi
sudo usermod -aG <grup_adı> <kullanıcı_adı>
# Örneğin: sudo usermod -aG sudo ahmet

# Kullanıcı Silme
sudo deluser <kullanıcı_adı>
# Örneğin: sudo deluser ahmet

# Kullanıcı Şifresini Değiştirme
sudo passwd <kullanıcı_adı>
# Örneğin: sudo passwd ahmet

# Kullanıcı Bilgilerini Görüntüleme
id <kullanıcı_adı>
# Örneğin: id ahmet 

# Kullanıcı Arasında Geçiş

# su Komutu
su - kullanici_adı
# Örneğin: su - ahmet

# dos2unix hatasi icin
sudo apt-get install dos2unix
find . -type f -exec dos2unix {} \;
# sudo Komutu
sudo -u kullanici_adı komut
# Örneğin: sudo -u ahmet ls

# Kullanıcı Oturumunu Değiştirme

# -l seçeneğiyle
su -l kullanici_adı
# Örneğin: su -l ahmet

# --login seçeneğiyle
su --login kullanici_adı
# Örneğin: su --login ahmet

# Eğer root olarak giriş yapamıyorsanız ve "xxxxxx" kullanıcısına sudo yetkileri vermeniz gerekiyorsa, aşağıdaki adımları takip edebilirsiniz. 
su -
nano /etc/sudoers
xxxxxx ALL=(ALL:ALL) ALL
exit

#Grup Üyeliklerini Kontrol Etme:
id <user>
Bu komut, kullanıcının grup üyeliklerini ve diğer bilgilerini gösterir.


