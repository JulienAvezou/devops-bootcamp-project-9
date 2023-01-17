# devops-bootcamp-project-9
Demo for module 12 - Terraform

A) Automate provisioning EC2

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

-----

B) Modules

1. Create folder structure for modules

- root module with resources, outputs, variables and providers living in their own separate files + child modules living in the modules folder > own folder also with their own resources, outputs, variables and providers files

![Capture d’écran 2023-01-17 à 18 12 00](https://user-images.githubusercontent.com/62488871/212966997-3eb3d975-2e05-4339-b401-b1d931ce0390.png)

2. Group all resources into logical units - for example 'subnet' related

![Capture d’écran 2023-01-17 à 18 18 30](https://user-images.githubusercontent.com/62488871/212968603-348ca146-e538-4f1a-b7f7-83461128a65a.png)

- can then import and use module by referencing that module in other modules

3. Use variables as inputs

![Capture d’écran 2023-01-17 à 18 18 45](https://user-images.githubusercontent.com/62488871/212968821-255977bc-c9e7-4abb-8808-b61caf31dd6e.png)

![Capture d’écran 2023-01-17 à 18 19 03](https://user-images.githubusercontent.com/62488871/212968854-a7555b5e-063b-4dca-a51d-c177a78b0e18.png)

4. Use values as outputs

![Capture d’écran 2023-01-17 à 18 25 47](https://user-images.githubusercontent.com/62488871/212969495-74a0a190-8b3f-4115-b948-58d3fb0fb893.png)

![Capture d’écran 2023-01-17 à 18 26 20](https://user-images.githubusercontent.com/62488871/212969539-8faa712a-6931-4a96-a6db-d374e909ca3b.png)

5. Run terraform init, then terraform plan to check for errors, then apply the changes and check that resources are created properly

![Capture d’écran 2023-01-17 à 18 31 04](https://user-images.githubusercontent.com/62488871/212970528-fdec737c-7506-4375-998a-429d5cd41548.png)

![Capture d’écran 2023-01-17 à 18 31 27](https://user-images.githubusercontent.com/62488871/212970564-77d4086f-de88-4969-a6d7-d04d34153c19.png)

6. Repeat above steps for additional modules you want to create, example 'webserver'

-----
