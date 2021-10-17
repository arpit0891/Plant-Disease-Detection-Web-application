For Linux
```

git clone https://github.com/arpit0891/Plant-Disease-Detection-Web-application.git

cd ./Plant-Disease-Detection-Web-application/'Web application'

sudo pip install -r requirements.txt

sudo docker build -t pdd .

sudo docker images --filter reference=pdd

sudo docker run -t -i -p 8080:8080 pdd

```
