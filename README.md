### [Summary]
sharing files with others is very popular on websites and instant messaging systems.This paper propose a new way that attacks targets by shared image files.An attacker are capable to determine whether a specific victim is visiting an attacker-controlled website because shared images are exempted from the same origin policy.This is what previous methods can not achieve.Because of diverse mix of implementattion strategies that websites choose,the leaky image attack also designed several to correspond each condition.However,the main subjects are identical:sever,browser and users.Consequently，paper present three direction to mitigate this issue:modifying the server-side implementation of an image sharing service, forbidding browsers from send cookies with third-party as default behavior and empowering the users with tools.

### [Main idea]
The leak is possible because images are exempted from the same-origin policy, and  image sharing services authenticate users through cookies。Shared files leak information because an attacker can determine whether a specific person is visiting an attacker-controlled website by checking whether the browser can access an image shared with this person

### [Challenge]
+ Websites,in real world,take different strategies of URLs and authentication,which has various combination and leads to complicated scenarios needed corresponding method.Besides,targets also divided into two direction:a specific one and a group.

+ When targets are a group of users,it is naive to share one image with each of the group as the attack has O(n) complexity both in number of leaky images and in number of requests.Apparently,this approach does not scale well to larger sets of users.
### [Strength]
+ This paper presents several scenarios of web attacks by leaky images.Specifically,each scenario corresponds type of threat，attacker and what attacker can achieve.Particularly,enumerating above information in a table is so distinct that readers are capable to understand paper.

+ Some privacy-aware users may disable Javascript to prevent Javascript code from obtain identity.Consequently,paper present a variant of leaky image attack based on pure HTML code to against the above scenario.
### [Weakness]
- All these attacks have complex or rigorous prerequisite even some of them are desired behaivor that websites would like to see.Fors example，victim and the attacker,in GitHub,are requested to share a private repository whereas attacker,who needs to log in Github and gets granted by victim,are able to access the images.

- In sectionⅡ，the introduction of same-policy concentrate on why any script loaded from one origin is not allowed to access parts of DOM loaded from another origin.It is better to highlight why images is exempted  from this policy to help readers understand why authors choose image as medium.
