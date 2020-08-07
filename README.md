# DEVOPS_TASK-1

## TASK OBJECTIVE:-

* **JOB-1**. If developer push to `dev`branch then jenkins will fetch from dev and deploy on dev-docker environent..
* **JOB-2**. If developer push to `master` branch then jenkins will fetch from master and deploy on master-docker environent,both dev-docker & master-docker                                      environment are on different containers..
* **JOB-3**. Manually the QA(Quality Assurance) team will check(test) for the website running in the dev-docker environment.If it is running fine,then jenkins will merge the dev branch to master branch..

### _PREREQUISITE_:-
                   * RHel-8 * Docker * Gitbash * Github * Jenkins 
                   

### Step by Step Process as Follow:-

* _**First of all i created a Repository on `Github` ,named as `DevopsTask1` and also initialised with readme**_ 


![github](https://user-images.githubusercontent.com/64469896/89687854-8f9e8b80-d91e-11ea-981d-1d253438b41e.png)

>Firstly i implemented JOB-2 :-

* _**On Gitbash (master branch),firstly i cloned my repository ,from github and then created an html file and edited on notepad,named as `ronak.html`**_..

![gitbash](https://user-images.githubusercontent.com/64469896/89688568-16a03380-d920-11ea-910a-7f029b9ca1e0.png)

* _**After creating a file,i pushed(uploaded) my file in github**_..

![gitbash](https://user-images.githubusercontent.com/64469896/89690140-72b88700-d923-11ea-87c0-4638c420d907.png)

![gitbash](https://user-images.githubusercontent.com/64469896/89690148-777d3b00-d923-11ea-82fb-b45eae5b43ff.png)

**html file has been uploaded on github**!!

![github](https://user-images.githubusercontent.com/64469896/89690431-1c981380-d924-11ea-84dc-89762f415a77.png)

* _**On rhel-8,i created a directory named as `master` and then created one folder named as production on which jenkins will copy file and also created a Dockerfile in which i created my own customized image,from which container launched**.._

**Before starting anything on rhel-8,i started docker and jenkins services,because both docker and jenkins are running on the top of rhel-8 and also disabled firewalld**..

![rhel8](https://user-images.githubusercontent.com/64469896/89693419-0d1cc880-d92c-11ea-8509-35fad55449c1.png
)

* _**On jenkins,firstly i installed github plugin and created a JOB,named as `job2(master-docker)env` and then configured it**_..

![jenkins1](https://user-images.githubusercontent.com/64469896/89694080-258de280-d92e-11ea-8347-849e66d8220c.png)

![jenkins2](https://user-images.githubusercontent.com/64469896/89694083-2b83c380-d92e-11ea-9306-7237b3ff94ff.png)

![jenkins3](https://user-images.githubusercontent.com/64469896/89694094-32aad180-d92e-11ea-8a0c-715237ae75b2.png)

**After configuration of job2,i build it and here is console output**

![jenkins4]()

**After putting IP of rhel8 with port no.8089(for production system),website deployed on webserver successfully....**

![output](https://user-images.githubusercontent.com/64469896/89695081-62f36f80-d930-11ea-8abe-886251ff2f3a.png)


