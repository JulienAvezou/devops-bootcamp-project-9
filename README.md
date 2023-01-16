# devops-bootcamp-project-9
Demo for module 12 - Terraform

1. Create vpc & subnet 

![Capture d’écran 2023-01-16 à 08 46 46](https://user-images.githubusercontent.com/62488871/212624377-96950122-188a-4b3b-99a7-6353b298993d.png)

![Capture d’écran 2023-01-16 à 08 46 56](https://user-images.githubusercontent.com/62488871/212624416-5f6a154c-64a0-4894-be69-58647b997032.png)

terraform apply
![Capture d’écran 2023-01-16 à 08 47 18](https://user-images.githubusercontent.com/62488871/212624435-d8f17b25-bffa-4ec0-8914-b121d6aa726a.png)

![Capture d’écran 2023-01-16 à 09 06 35](https://user-images.githubusercontent.com/62488871/212627917-69888c1f-8c72-424f-b403-1fb5410ae24e.png)

![Capture d’écran 2023-01-16 à 09 06 46](https://user-images.githubusercontent.com/62488871/212627943-15cf0716-2ba5-4ce4-98a2-2ad8928609ae.png)

2. Create Internet Gateway & connect to route table for vpc

![Capture d’écran 2023-01-16 à 09 08 06](https://user-images.githubusercontent.com/62488871/212628050-a25f409e-eb88-4df1-88a2-9c56878f19e6.png)

terraform apply

![Capture d’écran 2023-01-16 à 09 04 59](https://user-images.githubusercontent.com/62488871/212628148-5062332e-f731-441c-8528-86eabda69c9d.png)

![Capture d’écran 2023-01-16 à 09 05 15](https://user-images.githubusercontent.com/62488871/212628190-64298892-dd8c-428c-8155-aa14d941e685.png)

3. Associate subnet with correct route table so that subnets will be exposed via internet gateway

![Capture d’écran 2023-01-16 à 09 12 44](https://user-images.githubusercontent.com/62488871/212630202-5f56889b-9962-47fe-b9e1-1fc4c313011a.png)

![Capture d’écran 2023-01-16 à 09 12 54](https://user-images.githubusercontent.com/62488871/212630248-38262bc8-ba34-481c-9b87-3da4a8ea8ab6.png)

![Capture d’écran 2023-01-16 à 09 20 22](https://user-images.githubusercontent.com/62488871/212630327-c9d8b7d4-e039-4554-bc22-34b8de5b7f40.png)

4. Create security group with firewall rules

![Capture d’écran 2023-01-16 à 09 28 58](https://user-images.githubusercontent.com/62488871/212632185-b6f06eea-de48-444d-b25a-80c89a51010a.png)

![Capture d’écran 2023-01-16 à 09 29 08](https://user-images.githubusercontent.com/62488871/212632210-da693921-5073-4c1b-a6d3-f118b5f6bb1a.png)

![Capture d’écran 2023-01-16 à 09 29 55](https://user-images.githubusercontent.com/62488871/212632239-455bc029-04cd-4718-94ff-4d4a5ee63376.png)

5. Create EC2 instance

![Capture d’écran 2023-01-16 à 17 05 56](https://user-images.githubusercontent.com/62488871/212721937-6cb3609e-4e62-45b7-b10f-3e95f8d05ea6.png)

![Capture d’écran 2023-01-16 à 17 06 05](https://user-images.githubusercontent.com/62488871/212721975-1b80c87c-b969-4825-a370-3229d16a4b8a.png)

![Capture d’écran 2023-01-16 à 17 06 30](https://user-images.githubusercontent.com/62488871/212722005-51996362-2815-4ffc-a278-d90fc48bedf4.png)

6. Script setup of server - docker nginx installations and running. Check that can access from browser

![Capture d’écran 2023-01-16 à 17 45 56](https://user-images.githubusercontent.com/62488871/212729659-11c6bdd0-723c-4bc9-bbbd-7919d547386c.png)

![Capture d’écran 2023-01-16 à 17 46 03](https://user-images.githubusercontent.com/62488871/212729684-61463f54-78cc-491f-afc2-5f286fc8fd26.png)

<img width="715" alt="Capture d’écran 2023-01-16 à 17 40 26" src="https://user-images.githubusercontent.com/62488871/212729720-b4999556-3630-485b-a5e8-653e55924140.png">













