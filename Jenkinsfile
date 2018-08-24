   node('jenkins') {
       
        stage('clone repository'){
        checkout scm
    }
    
    
          stage('create deployement  k8s'){
              withKubeConfig(caCertificate: '', credentialsId: '997a5473-5f78-4e75-a2c3-ec38bcb64364', serverUrl: '127.0.0.1:8001') {
    // some block
    
    stage('create deployement for mariadb'){
     
     sh 'kubectl create -f MariaDB.yaml'
     sh 'kubectl create -f volume-mariadb.yaml'     
    }
    
     stage('create deployement for glpi'){
     sh 'kubectl get pods' 
     sh 'kubectl create -f Glpi.yaml'
     sh 'kubectl create -f volume-hpg.yaml'     
    }
    
     sh 'kubectl get pods' 
    
}
               
            }
            
              
            }
