Yani bu depo ile bilgisayarında çalışmak, değişiklik yapmak, güncellemek (push/pull) istiyorsun.
Aşağıda bu depoyla ilgili tüm temel Git işlemlerini adım adım ve çalışır şekilde verdim 👇

🔹 1. Depoyu bilgisayarına indirme (clone)

Önce projeyi bilgisayarına almak için terminal (Git Bash) aç ve şunu yaz:

cd Desktop  # veya istediğin klasör
git clone https://github.com/halil2023/web.git


Bu komut, web adında bir klasör oluşturur.

👉 Artık bu klasörde projenin tüm dosyaları olacak.
Gir:

cd web

🔹 2. Dosya değiştirme

Klasördeki dosyaları düzenle (örneğin index.html, style.css vs.)
Sonra değişiklikleri Git’e kaydetmek için şu 3 adımı uygula:

git add .
git commit -m "Yeni düzenleme yapıldı"
git push


✅ Bu komutlar değişikliklerini GitHub’daki https://github.com/halil2023/web deposuna gönderir.

🔹 3. Depoyu güncellemek (pull)

Başka biri (veya sen başka bir bilgisayarda) değişiklik yaptıysa ve sen son halini almak istiyorsan:

git pull


Bu komut GitHub’daki son güncellemeleri bilgisayarına çeker.

🔹 4. Yeni dosya ekleme

Yeni dosya (örnek: script.js) eklediysen yine şu komutlar:

git add .
git commit -m "script.js eklendi"
git push

🔹 5. Git durumu kontrol etme

Ne değişmiş, ne eklenmiş görmek için:

git status

🔹 6. Bağlantıyı kontrol et

Depo bağlantısını görmek için:

git remote -v


Eğer yanlışsa (örneğin başka hesaba bağlıysa) düzelt:

git remote remove origin
git remote add origin https://github.com/halil2023/web.git

🔑 7. İlk defa push yaparken kimlik isterse

GitHub artık şifre değil, Access Token kullanıyor.

Token oluşturmak için:
1️⃣ GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
2️⃣ “Generate new token → classic”
3️⃣ repo kutusunu işaretle
4️⃣ Token’ı kopyala
5️⃣ Terminalde kullanıcı adı → halil2023
6️⃣ Şifre → Token’ı yapıştır

🔹 8. Yeni dal (branch) oluşturma (isteğe bağlı)

Yeni bir özellik veya deneme yapmak istiyorsan:

git checkout -b deneme


Sonra:

git add .
git commit -m "deneme dalı eklendi"
git push -u origin deneme

✅ Özet
İşlem	Komut
Depoyu klonla	git clone https://github.com/halil2023/web.git
Dosya ekle	git add .
Commit yap	git commit -m "mesaj"
GitHub’a gönder	git push
Güncelleme al	git pull
Durumu gör	git status
