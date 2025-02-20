<h1>TWS - DevOps Hackathon - Phase 1</h1>
<hr><p>Small E-Commerce React/Vite/Docker Project</p><h2>General Information</h2>
<hr><ul>
<li>In this project you have to host the app in any cloud provider and while doing that you have to use linux, git and docker concepts to host and run the application.</li>
</ul><ul>

<li>It help you to learn basic Cloud/DevOps skills, like Linux/Git/Docker</li>

</ul><h2>Technologies Used</h2>
<hr><ul>
<li>React</li>
</ul><ul>
<li>VITE</li>
</ul><ul>
<li>Docker</li>
</ul><ul>
<li>Linux</li>
</ul><h2>Setup</h2>
<hr><p>First tried and installed on local linux environment, Update/Install $apt then installed docker and created the docker image with node 18 image but it did not worked. Then searched on the internet and found i need to also install the vite npm package.</p><h5>Steps</h5><ul>
<li>Install/login/fork and pull the repo.</li>
</ul><ul>
<li>Update linux packages with apt update and upgrade.</li>
</ul><ul>
<li>Install Docker.io package with apt install docker.io</li>
</ul><ul>
<li>Create Dockerfile with all the config</li>
</ul><h2>Usage</h2>
<hr><p>#Base Image
FROM node:18</p>
<p>#Working Dir
WORKDIR /app</p>
<p>#Copy the packages from app folder
COPY package*.json ./</p>
<p>#Install Dependencies
RUN npm install</p>
<p>#As it also require Vite, tried erlier but it did't worked so searched on net
RUN npm install -g vite</p>
<p>#Copy rest of the files
COPY . .</p>
<p>#Expose the port of the app
EXPOSE 5173</p>
<p>#Start the server
CMD ["npm", "run", "dev"]</p><h5>Code Examples</h5><ul>
<li>You have to make a Docker image after creating the Dockerfile and then run the created image with mentioning the -d for detatched -p for mapping host port 300 with the app port(vite) 5173 and check the docker status. Open the inbound connection on port 3000 on the cloud provider.</li>
</ul><h2>Contact</h2>
<hr><p><span style="margin-right: 30px;"></span><a href="https://www.linkedin.com/in/shiveshkumar03/"><img target="_blank" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" style="width: 10%;"></a><span style="margin-right: 30px;"></span><a href="https://github.com/shivesh-kumar03"><img target="_blank" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" style="width: 10%;"></a></p>
