## ElasticBeanstalk

- create a Beanstalk environment: from the terminal run `eb init udagram-api --platfom node.js --region us-east-1`

- create environment sample: run `eb create --sample udagram-api-dev`

- from AWS console search for `eb` and choose `Elastic Beanstalk` you will find the environment we just created

  ![eb created](../../screenshots/ElasticBeanstalk/EB1.png)

  ![eb created](../../screenshots/ElasticBeanstalk/EB2.png)

- the endpoint is working fine

  ![eb endpoint](../../screenshots/ElasticBeanstalk/EB3.png)

- now we need to deploy our project: from your project run `eb use-udagram-api dev` on the terminal

- build the application `npm run build`

- to set the environment variables run `eb setenv <key>=<value>`

- run `eb deploy udagram-api-dev`
  ![eb endpoint](../../screenshots/ElasticBeanstalk/EB4.png)

- then check our environment from the AWS console

  ![eb endpoint](../../screenshots/ElasticBeanstalk/EB5.png)
