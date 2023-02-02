Continous Integration [CI] Flow:
--------------------------------
1- Developer write the code, make the changes to the code and tested locally.

2- Developer will be integrated with VCS like GitHub.
	
3- Push the code GitHub Repo.

4- Here come Jenkins will detect the code change and fetch the code.

5- The code will be build using Maven as souce code is Java Code.

6- This will generte Artifacts.

7- Conduct Unit Test again with Maven [Unit Test Framework.
	- Unit Test will be part of souce code.
	- Generte some reports in XML Format.

8- Conduct another type of test called Code Analysis using SonarQube and CheckStyle.
	- To checj if the code has any vulnarbilties.
	- Check any bugs ?
	- Following the best practices ?
	- And many other parameters to analyse your code.

9- This Code Analysing will genertae some reports in XML format which will uploaded in SonarQube Server.
	- SonarQube Server gives you more features to detect more informations
	- Quality Gate can be configured to control the build process [ If this code doesn't follow certain practices so fail the build to stop the pipeline ]


10- If it passes these testing process you will have a verified copy of the Artifact uploaded.	

11- Before we  depoly the Artifact on a server this Artifact will be versioned and pushed to Nexus Repo.

12- Code post Notification:
	- Integrate Jenkins with Slack and notify member with the status of the pipeline.
