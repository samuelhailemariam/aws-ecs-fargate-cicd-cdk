## CI/CD DEPLOYMENT ON ECS

Deploy infrastructure (**ECS** cluster fronted by Application LoadBalancer) and a CI/CD pipeline (**AWS CodePipeline**) using **AWS Cloud Development Kit (CDK)** with Python. The CodePipleline is automatically triggered on push events to a designated repo and will containerize the web-based application and push the new image to Amazon Container Registry (ECR). The image is then deployed to Amazon ECS Fargate cluster once the manual approval stage in CodePipeline is approved.

#### Running Code:

1. Create a virtualenv on MacOS and Linux:

```
$ python3 -m venv .venv
```

2. Activate your virtualenv.

```
$ source .venv/bin/activate
```

3. Install the required dependencies.

```
$ pip install -r requirements.txt
```

4. Synthesize the CloudFormation template.

```
$ cdk synth
```

#### Useful commands

- `cdk ls` list all stacks in the app
- `cdk synth` emits the synthesized CloudFormation template
- `cdk deploy` deploy this stack to your default AWS account/region
- `cdk diff` compare deployed stack with current state
- `cdk docs` open CDK documentation
