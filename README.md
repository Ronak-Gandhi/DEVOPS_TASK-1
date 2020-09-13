# DEVOPS_TASK-1

## TASK OBJECTIVE:-

* **JOB-1**. If developer push to `dev`branch then jenkins will fetch from dev and deploy on dev-docker environent..
* **JOB-2**. If developer push to `master` branch then jenkins will fetch from master and deploy on master-docker environent,both dev-docker & master-docker                                      environment are on different containers..
* **JOB-3**. Manually the QA(Quality Assurance) team will check(test) for the website running in the dev-docker environment.If it is running fine,then jenkins will merge the dev branch to master branch..

### _PREREQUISITE_:-
                   * RHel-8 * Docker * Gitbash * Github * Jenkins 
                   

### Step by Step Process as Follow:-

* _**First of all i created a Repository on `Github` ,named as `DevopsTask1` and also initialised with readme**_ 


![github](https://user-images.githubusercontent.com/64469896/90269190-ddaf1400-de75-11ea-883e-4e6140f42457.png)

---

>## _Firstly i Implemented `JOB-2`_ :-


* _**On Gitbash (master branch),firstly i cloned my repository ,from github and then created an html file and edited on notepad,named as `ronak.html`**_..

![gitbash](https://user-images.githubusercontent.com/64469896/89688568-16a03380-d920-11ea-910a-7f029b9ca1e0.png)

* _**After creating a file,i pushed(uploaded) my file in github**_..

![gitbash](https://user-images.githubusercontent.com/64469896/89690140-72b88700-d923-11ea-87c0-4638c420d907.png)

![gitbash](https://user-images.githubusercontent.com/64469896/89690148-777d3b00-d923-11ea-82fb-b45eae5b43ff.png)

**html file has been uploaded on github**!! (master branch)

![github](https://user-images.githubusercontent.com/64469896/89690431-1c981380-d924-11ea-84dc-89762f415a77.png)

* _**On rhel-8,i created a directory named as `master` and then created one folder named as production on which jenkins will copy file and also created a Dockerfile which build the image,from which container launched**.._

**Before starting anything on rhel-8,i started docker and jenkins services,because both docker and jenkins are running on the top of rhel-8 and also disabled firewalld**..

![rhel8](https://user-images.githubusercontent.com/64469896/89693419-0d1cc880-d92c-11ea-8509-35fad55449c1.png
)

![rhel8](https://user-images.githubusercontent.com/64469896/90289322-41970400-de99-11ea-9163-258535c0455b.png)


* _**On jenkins,firstly i installed github plugin and created a JOB,named as `job2(master-docker)env` and then configured it**_..

![jenkins1](https://user-images.githubusercontent.com/64469896/89694080-258de280-d92e-11ea-8347-849e66d8220c.png)

![jenkins2](https://user-images.githubusercontent.com/64469896/89694083-2b83c380-d92e-11ea-9306-7237b3ff94ff.png)

![jenkins3](https://user-images.githubusercontent.com/64469896/89694094-32aad180-d92e-11ea-8a0c-715237ae75b2.png)

![jenkins4](https://user-images.githubusercontent.com/64469896/89697853-c20ab180-d93b-11ea-8edd-6bbf6c1ccf9f.png)

**After configuration of job2,i build it and here is console output**

![jenkins4](https://user-images.githubusercontent.com/64469896/89697858-c6cf6580-d93b-11ea-8613-21d0b1e3b304.png)

**After putting IP of rhel8 with port no.8089(for production environment),website deployed on webserver successfully....**

![output](https://user-images.githubusercontent.com/64469896/89695081-62f36f80-d930-11ea-8abe-886251ff2f3a.png)

---

>## _Implementation of job-1_ :-


* _**On Gitbash(dev branch), i added some more lines on the same html file and then uploaded on github**_..

![gitbash1](https://user-images.githubusercontent.com/64469896/89695625-5a9c3400-d932-11ea-98aa-34d36081597f.png)

![gitbash2](https://user-images.githubusercontent.com/64469896/89695639-625bd880-d932-11ea-8acc-b3624c6ca0d0.png)

**html file has been uploaded on github**!! (dev branch)

![github](https://user-images.githubusercontent.com/64469896/89695906-5b819580-d933-11ea-999b-a63c3da0efc9.png)


* _**On rhel-8,i again created a directory named as `dev` and then created one folder named as testing on which jenkins will copy file and also created a Dockerfile which build the image,from which container launched**.._


![rhel8](https://user-images.githubusercontent.com/64469896/89696531-ebc0da00-d935-11ea-808e-24121b559f11.png)

![rhel8](https://user-images.githubusercontent.com/64469896/90269256-fe776980-de75-11ea-8df7-297745e54bcc.png)




* _**On jenkins,i again created a JOB,named as `job1(dev-docker)env` and then configured it**_..

![jenkins1](https://user-images.githubusercontent.com/64469896/89697866-d058cd80-d93b-11ea-97a1-111220827eab.png)

![jenkins2](https://user-images.githubusercontent.com/64469896/89698074-d602e300-d93c-11ea-9707-67d93806ed8c.png)

![jenkins3](https://user-images.githubusercontent.com/64469896/89697947-3ba29f80-d93c-11ea-9e73-adab360af595.png)


**After configuration of job2,i build it and here is console output**

![console](https://user-images.githubusercontent.com/64469896/89697953-41988080-d93c-11ea-8d84-8d77fee90845.png)

**Now the Quality Assurance(QA) team manually check,if website running fine or not,,After putting IP of rhel8 with port no.8082(for testing environment),website deployed on webserver successfully....**

![output](https://user-images.githubusercontent.com/64469896/89696845-46a70100-d937-11ea-835a-50ee9b3cd708.png)

---

>## _Implementation of job-3_ :-


* _**On jenkins,i again created a JOB,named as `job3(merge)` and then configured it**_..

![jenkins1](https://user-images.githubusercontent.com/64469896/89697968-5543e700-d93c-11ea-92f6-aaa82353ff13.png)

![jenkins2](https://user-images.githubusercontent.com/64469896/89697970-5aa13180-d93c-11ea-8772-fe522b622953.png)

![jenkins3](https://user-images.githubusercontent.com/64469896/89697976-60971280-d93c-11ea-86ac-7508bea38879.png)


**After configuration of job3,i build it and here is console output**..

![console](https://user-images.githubusercontent.com/64469896/89697140-6be83f00-d938-11ea-982e-ceb6c48d2f3b.png)

**After putting IP of rhel-8 with port no.8082(production environment),because we merged dev into docker and it deployed successfully**..

![output](https://user-images.githubusercontent.com/64469896/89697288-22e4ba80-d939-11ea-9422-5d7396b87a1c.png)


## THANK YOU !!
