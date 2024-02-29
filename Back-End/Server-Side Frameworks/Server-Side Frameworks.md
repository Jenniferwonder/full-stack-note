---
Title: Server-Side Frameworks
Type: Note
tags: TechSkills
DateStarted: 2023-03-06
DateModified: 2023-07-04
status:
DateDo:
DateDue: 
DateDone:
Total: 0
Completed: 0
Incomplete: 0
sr-due: 2023-07-02
sr-interval: 4
sr-ease: 273
---
- Up:: [[Back-End Basics]]
## Server-Side Framework

- DX-developer experience
- Set-up

#### 1. Routing

- Provide **routing** that can map a URL in the browser to code you want to run on the server

#### 2. Database integration

- Provide an abstraction over your relational database
  - Have **built-in object relational mapper** that can migrate code from your preferred programming language into SQL code that can be used by the database

#### 3. Architecture

- Provide a way to dynamically insert data from your database into HTML  
  ❗The framework you choose is going to dictate your life for the next 10 years.  
  Together, they make MVC, the most common approach when building a full-stack web app.

## Server-Side Framework Choices

![[zz-assets/Pasted image 20230308194505.png]]

- Go Gin [https://gin-gonic.com/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbTAzakYtRWZjRElhaVlkcmdfMzh0bUNHcHF5QXxBQ3Jtc0trVmxodWhiM004X3MxbmlGdFZiVlNzN2IwQzgyUDJqdzBMU2FRZTZ3M0JLSVFPWDh3T01hOUVoTGRHYUd2c2ZWdzB2VFduS3RsZFVMU0swU2hubTJReUV4VS14NTlYbktGMzdySV85ckFpSFJfT090OA&q=https%3A%2F%2Fgin-gonic.com%2F&v=FQPlEnKav48)
- Swift Vapor [https://vapor.codes/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbkdFa2xHb3J4UEphMzloQVZRbUltZ2NwbnlXQXxBQ3Jtc0ttVG5uMndsWjFYTjZwR0FVc0NMUktmLTlsYktlNG9VYmRHVnBZWFZJbU1pUi0zSHhsSUthWkdsSnptSmJORTJwekhsYTA5VU1ZT24xUkRJbnBmVVBLTVlsSFYzaDVrdVVEZHVjbjdsSXFhZzZLd0F1MA&q=https%3A%2F%2Fvapor.codes%2F&v=FQPlEnKav48)
- Java Spring [https://spring.io/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbG52Nm82VnA5M2hMUVAtc1M4ZkpoV0lCUEV2d3xBQ3Jtc0tuUHllNE41WG1HOUl6QlZBdlRSSWYtVkdocEdfSzRLRXdJcjM3bkFYSk1ieXFUa1dOb1JrcktWZjEtSTJBMi1ZTzJ1NC05TnFjbThOOGVadUNMeG42UWh0czRQVXBKZ2V1NEV4OG00ZFI5OEFGRDV0NA&q=https%3A%2F%2Fspring.io%2F&v=FQPlEnKav48)
- Ruby on Rails [https://rubyonrails.org/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbkNEYjhOQnhaZjA4MGRybnhRUUFaSjBSRTI5Z3xBQ3Jtc0tuT2pQRHh5NFJfT2U0cDBGT2NyN1hDc0JOd01peWZCR21oVHZiR2FHZHo0TDBXRnY3TEotTWc3YVRrYjZyamVrRUtlZE9XRDJyV0xUYzdwZ21Gb3hZT3VjdFZ2UG9MVGhnZDFyOEVIM1RuWWFRT3Fhaw&q=https%3A%2F%2Frubyonrails.org%2F&v=FQPlEnKav48)
- Python Django [https://djangoproject.com](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbjE2a0pYeUlqeHBMSTByWG9BTkxvSWx5X1QwZ3xBQ3Jtc0ttQTFqTmtmLWE5XzBfeGZPZnJJZTc2SXpjdGZuMUt3dFduNDBSS1lCdE5HbnNZN19FcEhaT3pKUFZVNlByTmxaRFkta1BNc0tLaTcwVkVHbUpXVVZUVTlhMlU3T3JJZWhRNlRYSjFYRnhiRkJMMHV3cw&q=https%3A%2F%2Fdjangoproject.com%2F&v=FQPlEnKav48)
- PHP Laravel [https://laravel.com/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbUJCdjF3VVl2VGl1VFNOS19PYmlCOXVtQjZSd3xBQ3Jtc0tsbEJGS1EwVmNuSzRmbkRrVnY5N2hHU1dhbUV0U09yRWdqeVlfSTQ2NU9GYlk2MF9DVU5DQ0VCTTNrbk9JNVkwVG52UEp4aHlEdXNXQm5OMDlBUDBLdnJINzM3bk0wdEhmc3dwSUtSd0NqU21hZ29jYw&q=https%3A%2F%2Flaravel.com%2F&v=FQPlEnKav48)
- C# .NET [https://dotnet.microsoft.com/en-us/ap...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbmhRWTRJSG94T3otM1lfWGxFeVhCelYyLXJrd3xBQ3Jtc0trdFcxUWowdFpqbk9YLXpBQ213YUxXY1hlbmxyQTlwMV9mYUdzcDF0c2VLZ2lDYmotN0V4a2ZhcE4yT3dpdkx4OHoyVW5vSmN3Q0RTRVo5ODBSbFlKN05vMUFCNU85cnZldXJEc1JQQmpiOUJwM0ZNNA&q=https%3A%2F%2Fdotnet.microsoft.com%2Fen-us%2Fapps%2Faspnet&v=FQPlEnKav48)
- Elixir Phoenix [https://phoenixframework.org/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbkNMakNUd3pNVlFlR3FKU2ZsLUxSMWZubm9PUXxBQ3Jtc0tuOGh1RFI4Y3NuYzJrbUVXN0d0NnpqSUZJQ1R4cGk4YXZWQ1E2YkxDZU5wckp4ZkpBZDVTbkJOT0tRTlV0XzNianVPRXAyNENDQ2FyZ3QwRkVuWGE2aFlaUjJ4MGVTaVk5blNHN2hsVlpBY1FEaWxyZw&q=https%3A%2F%2Fphoenixframework.org%2F&v=FQPlEnKav48)
- Rust Rocket [https://rocket.rs/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbUFIUF9WRGxoQ0Foc250OVF6UVpMcEpOSV9IZ3xBQ3Jtc0ttYy1WZmJScnU1UkYxbmtYemhUMUE2NG1nRjhvWmlSV01rZEpGVDI0bngxSzN4Ni11bVVidnlMU1c1RDB6WmNCTm55aVVKRUg1bXFnV3JoZlQ0UFFNUjR6TXVkbFdCc0h2ekpwamNuSU9HOVo3SE1xUQ&q=https%3A%2F%2Frocket.rs%2F&v=FQPlEnKav48)
- Kotlin Ktor [https://ktor.io/](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqa2hZS3hsYWNjUmFHdUpYemlBbXB0SjFaZll4d3xBQ3Jtc0trRHpweml6NzNtUkdsX2YtSExycWRVVXdwakZkN3Rqc1RSNmVhLWtERE5uOWZxTzA1dDg2N08tMUVFRzZkUGpXUExCcXRKWlh5NWp0NXJ1bmVxMDcwZmdTSm9xeXZNUjNwbWR2Zlk0QlBpSFhPV0d6VQ&q=https%3A%2F%2Fktor.io%2F&v=FQPlEnKav48)
