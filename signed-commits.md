# İmzalı Commit (Signed Commits) Nasıl Kullanılır?


Kullanıcılar, Git istemcilerini GPG veya S/MIME anahtarı ile commit'leri imzalayacak şekilde yapılandırarak **imzalı commit (signed commits)** özelliğini etkinleştirebilir. Adımlar:


1. GPG anahtarı oluşturun veya içe aktarın (ör: `gpg --full-generate-key` komutu ile).
2. Oluşturduğunuz GPG açık anahtarını GitHub hesabınıza ekleyin (GitHub > Settings > SSH and GPG keys).
3. Git'i bu anahtarı kullanacak şekilde yapılandırın:

```bash
git config --global user.signingkey <ANAHTAR_ADNIZ>
git config --global commit.gpgsign true
```

4. GPG'nin bilgisayarınızda kurulu ve PATH değişkeninde olduğundan emin olun.


Artık tüm commit'leriniz **imzalı commit (signed commits)** olacak ve GitHub üzerinde "Verified" (Doğrulandı) olarak görünecektir.

# Önemli Not

> **Topluluk depolarına commit atabilmek için imzalı commit (signed commits) kullanmak ZORUNLUDUR.**
> Bu gereklilik, topluluk güvenliğini ve yapılan değişikliklerin doğruluğunu sağlamak için uygulanmaktadır. İmzalı commit olmadan yapılan katkılar kabul edilmeyecektir.


