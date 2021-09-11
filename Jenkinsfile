node{
    
    stage("Checken"){
        git credentialsId: 'nitin_priv_key', url: 'git@github.com:nitinpeter/scripts.git'
    }
    stage("Cleanen"){
        sh '''#!/bin/bash
            for i in `find . -name \'*.py\'`; do echo $i; rm -f $i;done'''
        zip archive:true, dir: '',glob: '',zipFile: 'npscript.zip'
    }
    
}
