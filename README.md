# Web Container in Azure

This simple project builds an docker image from nginx and copies a simple web application content using html and css , Following are the steps to push the image to an azure container registery 

### Pre requirement 

You would need to have an Azure account with a available container registry .


### Build an docker image 
### ```docker build -t myprofile-image:v1.0 .```

### Run it locally
### ```docker run -d -p 80:80 myprofile-image:v1.0```
### open localhost in an browser

## Login to azure 
### ```az acr login --name <container name>```

### Tag the image 
### ```docker tag myprofile-image:v1.0 <container name>.azurecr.io/images/myprofile```

### Push the image to azure container repo
### ```docker push <container name>.azurecr.io/images/myprofile```


