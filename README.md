# cross-selling

## 1. Install Docker Desktop

Download *Docker Desktop* from <link>https://www.docker.com/products/docker-desktop</link> and install it on your local machine.

## 2. Clone the repo to your local machine
open command window, run the following command <p>
```
git clone https://github.com/nbzhyekai/cross-selling.git
```
## 3. Build Docker Container
(a) Navigate to the project folder <p>
```
cd cross-selling
```
(b) Build Docker image<p>
```
docker build -t cross-selling:v20210317 -f Dockerfile .
```

(c) Run Docker image, run the following command and the argument *\<path to project folder\>* by the directory on your machine, e.g. *C:\cross-selling* <p>
```
docker run -d --name "cross-selling" --entrypoint "/bin/bash" -it -p 8888:8888 -v "\<path to project folder\>":/workspace/cross-selling cross-selling:v20210317
```
  
(d) Start the container <p>
```
docker start cross-selling
docker attach cross-selling
```
After running the command you are now in the container and should be able to see the following output: <p>
```
root@7298753620f1:/#
```
(e) Inside the container, install Jupyter lab
```
root@7298753620f1:/# pip install jupyterlab
```
(f) After installing, start Jupyter lab
```
root@7298753620f1:/# jupyter lab --ip=0.0.0.0 --port=8888 --allow-root
```  
(g) Open web browser, go to 
```
http://localhost:8888/lab
```  
paste the token in command window. You are able to run the code in Jupyter lab
  
