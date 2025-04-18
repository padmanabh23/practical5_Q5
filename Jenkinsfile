pipeline { 
agent any 
stages { 
stage('Clone Repository') { 
steps { 
git branch: 'main', url: 'https://github.com/padmanabh23/practical5_Q5.git' 
} 
} 
stage('Build Docker Image') { 
steps { 
dir('Q5') { 
script { 
docker.build("nodejs-app", ".") 
} 
} 
} 
} 
stage('Run Docker Container') { 
steps { 
script { 
docker.image("nodejs-app").run("-p 3000:3000") 
} 
} 
} 
} 
}
