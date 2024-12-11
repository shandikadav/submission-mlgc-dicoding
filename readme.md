<p align="center">
    <img src="https://media.tenor.com/o8ECtZBADOYAAAAM/liliel-25-dimensional-seduction.gif" height="281">
</p>

# Wassup, let's go kita deploy backend pake Cloud Run hehe 😆😆

1. Buka Google Cloud Cloud Shell lewat [Google Cloud Console](https://console.cloud.google.com/)
> Note : Jangan lupa gunakan project yang sesuai dengan ketentuan reviewer


2. Silahkan Clone terlebih dahulu project ini
```bash
git clone https://github.com/shandikadav/submission-mlgc-dicoding.git
```

3. Jangan lupa buat bucket untuk menyimpan modelnya dan silahkan copy linknya dan taruh di file .env


4. Build docker image lewat Dockerfile
 ```bash
docker build -t gcr.io/[PROJECT_ID]/[SERVICE_NAME] .
```

5. Push image ke Google Container Registry
```bash
 docker push gcr.io/[PROJECT_ID]/[SERVICE_NAME]
```

6. Tinggal deploy deh
```bash
   gcloud run deploy [SERVICE_NAME] \
    --image gcr.io/[PROJECT_ID]/[SERVICE_NAME] \
    --region [REGION] \
    --allow-unauthenticated
```

<br>

<p>Tunggu sebentar lalu selesai, nanti setelah berhasil di deploy tinggal taruh endpointnya ke bagian front end 🥳🥳</p>
