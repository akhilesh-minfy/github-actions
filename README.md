# github-actions
In this assignment we are making a pipeline to automate the running and installation of docker inside our EC2 instance and also the creating and building image and running the container firstly we need to create a docke hub image and create a new access token or password After this creation of access token we need to create a github repo with " CICD_PIPELINE " then upload all files app.js , package.json then run the
- create a ec2 intance with ssh and tcp 3000 inbound rule
  ![image (3)](https://github.com/user-attachments/assets/7a3ff549-724d-456d-8774-e99508937e52)
- ssh into that instance and install docker in it and give privilege to current user to run docker commands logout and login to apply this chanages
    ![image (2)](https://github.com/user-attachments/assets/e2e15791-e96f-4efb-bdb5-f35238002924)
![image (1)](https://github.com/user-attachments/assets/71b8a8df-4a90-49c8-a54f-4b9b5ded82df)
![image](https://github.com/user-attachments/assets/edb6d5a3-3d7a-48e7-acba-0d1df5272ff7)




# k8s-mongo-express
 ## 1. Handle the Password
- First handle the password securely.  use a Kubernetes Secret for this.
- create a secret.yaml file that holds your admin username and password (encoded in base64, of course) and then just kubectl apply it.
 ## 2. Launch the Database
- make a mongodb.yaml file to launch MongoDB and give it a stable network name so other apps can find it.
- to grab the password directly from the secret refer that secret.
 ## 3. Set Up the Config
- create ConfigMap. This is just a simple place to store the database's address, making it easy for our web UI to find it later.
## 4. Deploy the Web UI
- create  Mongo-Express. In another YAML file, we'll set up the web interface. We'll point it to our database using the ConfigMap and tell it how to log in using our secret. We'll also use that same secret to protect the web login page itself.
 ## 5. Access It
- everything should be running. You can check with kubectl get all.
To get the link, just run the command to expose the mongo-express-service. It'll give you a URL. Pop that into your browser, log in with the credentials you created, and you're in. You can now manage your database from the web.
 ## 6. Clean Up
- run kubectl delete on all the YAML files you used to create everything.

![Screenshot (36)](https://github.com/user-attachments/assets/5870c626-1367-486a-8817-406d1ca0a5e7)
![Screenshot (37)](https://github.com/user-attachments/assets/89a0a0cc-a016-4445-9c11-ef2c23d83bac)
![Screenshot (38)](https://github.com/user-attachments/assets/ed024474-26e0-444d-8597-9f66d8116ac4)
![Screenshot (39)](https://github.com/user-attachments/assets/f48b62cf-0340-4616-80a5-49343716cfe3)


