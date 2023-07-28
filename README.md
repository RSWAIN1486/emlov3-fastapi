______________________________________________________________________

<div align="center">

# FastAPI Demo with Docker

</div>

## Description

- Build and run scripted GPT and VIT model with FastAPI on Docker.
- Calculate average response time for 100 sequential requests.

### Build and launch FastAPI using Docker. This should launch demo at http://localhost:8080/ or http://<your-ec2-external-ip>:8080/
```bash
# for GPT
docker-compose  -f docker-compose.yml up --build demo_gpt

# for VIT
docker-compose  -f docker-compose.yml up --build demo_vit

```

### Generate a log file with individual and average response time for 100 api requests.
```bash
# for GPT. Set the server url and log file path accordingly.
python3 gpt/test_api_calls_gpt.py

# for VIT. Set the server url, input image file and log file path accordingly.
python3 vit/test_api_calls_vit.py

```

#### Average response time for GPT

<div align="left">

![image](https://github.com/RSWAIN1486/emlov3-fastapi/assets/48782471/39b7e473-588a-4956-b249-88aaca5bf8b0)

</div>

#### Average response time for VIT

<div align="left">

![image](https://github.com/RSWAIN1486/emlov3-fastapi/assets/48782471/6c564894-1ac6-4963-bace-d291aff77823)

</div>

#### CPU usage with 2 workers for GPT

<div align="left">

![image](https://github.com/RSWAIN1486/emlov3-fastapi/assets/48782471/2bff0f77-f7cd-4a6f-8e84-552824b78650)

</div>
