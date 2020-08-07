# DEVOPS_TASK-1

## TASK OBJECTIVE:-

* **JOB-1**. If developer push to `dev`branch then jenkins will fetch from dev and deploy on dev-docker environent..
* **JOB-2**. If developer push to `master` branch then jenkins will fetch from master and deploy on master-docker environent,both dev-docker & master-docker                                      environment are on different containers..
* **JOB-3**. Manually the QA(Quality Assurance) team will check(test) for the website running in the dev-docker environment.If it is running fine,then jenkins will merge the dev branch to master branch..

### _PREREQUISITE_:-
                   * RHel-8 * Docker * Gitbash * Github * Jenkins 
                   

### Step by Step Process as Follow:-

* _**First of all i created a Repository on `Github` ,named as DevopsTask1 and also initialised with readme**_ 


![github](https://user-images.githubusercontent.com/64469896/89687854-8f9e8b80-d91e-11ea-981d-1d253438b41e.png)

>**Firstly i implemented JOB-2**:-

* _**On Gitbash (master branch),firstly i cloned my repository ,from github and then created an html file and edited on notepad,named as ronak.html**_..

![gitbash](https://user-images.githubusercontent.com/64469896/89688568-16a03380-d920-11ea-910a-7f029b9ca1e0.png)

* _**After creating a file,i pushed(uploaded) my file in github**_..

![gitbash](https://user-images.githubusercontent.com/64469896/89690140-72b88700-d923-11ea-87c0-4638c420d907.png)
![gitbash]()
