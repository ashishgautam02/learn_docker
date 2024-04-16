====== Docker references


------ Building a NodeJS Docker file: 

### File Content

> FROM node
> WORKDIR /usr/app
> COPY package.json .
> RUN npm install
> COPY . .
> EXPOSE 8005
> CMD [ "npm", "start" ]

### Commands

#### - Build the image
```docker build -t fixytrade-be .```

#### - List all Images on System
```docker images```

#### - Run a specific image with PORT binding(8005<local>:8005<container>) and tag (-t)
```docker run -d -p 8005:8005 fixytrade-be```

#### - Kill a running image
```docker kill f454c7ff3e49```

#### - Force remove an image
```docker rmi -f fixytrade-be:latest```
