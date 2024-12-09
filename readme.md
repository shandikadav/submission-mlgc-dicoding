<p align="center">
  <img src="https://media1.tenor.com/m/ECjUDy1BiFEAAAAd/2%E9%BB%9E5%E6%AC%A1%E5%85%83%E3%81%AE%E8%AA%98%E6%83%91-nitengo-jigen-no-ririsa.gif" width="100%">
</p>

# Wassup, let's go kita deploy backend pake Cloud Run hehe 😆😆

1. Build docker image lewat Dockerfile
 ```bash
docker build -t gcr.io/[PROJECT_ID]/[SERVICE_NAME] .
```

2. Buat tag image untuk Google Container Registry
```bash
 docker tag [TAG_NAME] gcr.io/[PROJECT_ID]/[SERVICE_NAME]
```

3. Push image ke Google Container Registry
```bash
 docker push gcr.io/[PROJECT_ID]/[SERVICE_NAME]
```

4. Tinggal deploy deh
```bash
   gcloud run deploy [SERVICE_NAME] \
    --image gcr.io/[PROJECT_ID]/[SERVICE_NAME] \
    --tag [YOUR_TAG] \
    --region [REGION] \
    --allow-unauthenticated
```

## Tunggu sebentar lalu selesai, nanti setelah berhasil di deploy tinggal taruh endpointnya ke bagian front end 🥳🥳
