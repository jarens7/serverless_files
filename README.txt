In this challenge we use "Serverless" to setup, install, and update the node.js function.

Pre-requisites:
aws-cli installed and configured
S3 bucket and IAM role with permissions to update Lambda and S3

#Steps to get setup:
1. Install serverless
sudo nmp install -g serverless@beta
2. From within this repo, run:
serverless create aws-nodejs
npm install
3. Change your region and bucket name in "serverless.yml" to reflect the S3 bucket you will use and the region to setup in
4. Deploy
serverless Deploy
5. Testing, run the following command and feel free to change the URL to where the file is being grabbed from, and also change the data name to something relevant (also ignore image_url, this can be any file):
serverless invoke --function save --log --data="{ "image_url": "https://www.google.ca/url?sa=i&rct=j&q=&esrc=s&source=images&cd=&cad=rja&uact=8&ved=2ahUKEwiVkZ6nx9ndAhUTGTQIHWlyDOgQjRx6BAgBEAU&url=http%3A%2F%2Ffantendo.wikia.com%2Fwiki%2FFile%3ASmall-mario.png&psig=AOvVaw3r96wglO_jqDn7NgstycJ5&ust=1538081787449128", "key": "mario.png"
