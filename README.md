# SAP_Assignment

# QA_Assignment

## How to Run the project

## Pre-required
```
1) Install JDK 1.8 
2) Download selenium jar file selenium-server-standalone-3.141.59.jar (Its available in src/test/resource folder in project"
   Go to cmd and move to the directory where jar file is available and follow below steps
   ex:cd /Users/ravi.kne/Downloads then run below cmd to start hub
   java -jar selenium-server-standalone-3.141.59.jar -role hub

   Once the hub starts running, open the another cmd window and follow below steps to run node
   java -Dwebdriver.chrome.driver="/Users/ravi.kone/Documents/mobile/chromedriver" -jar selenium-server-standalone-3.141.59.jar -role  node -hub    http://192.168.1.4:4444/grid/register -port 5555 
  (192.168.1.4:4444/ this needs to be updated to your path which can seen in hub cmd window, so that hub can be rigistered with node)

3) To run test in Local System / Zelenium 

  # Go to Constants.java file and change the value of URl_source = "source-1"

  # To run Test in zelenium change value of URL_Source = "source-2"
  

4) Install the Zalenium by entering the cmds
    # Pull docker-selenium
    docker pull elgalu/selenium
    
    # Pull Zalenium
    docker pull dosel/zalenium
    
    # Run it!
    docker run --rm -ti --name zalenium -p 4444:4444 \
      -v /var/run/docker.sock:/var/run/docker.sock \
      -v /tmp/videos:/home/seluser/videos \
      --privileged dosel/zalenium start
      
    # Point your tests to http://localhost:4444/wd/hub and run them

    # Stop
    docker stop zalenium
    
```

Check if both installed properly in browser by entering below URLS
```
http://localhost:4444/grid/console  		[To check if Grib is running properly]
http://localhost:4444/grid/admin/live 		[To check if Zalenium is running properly]
http://localhost:4444/dashboard                 [To check if Zalenium dashboard]
```
