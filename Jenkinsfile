pipeline {
		agent {
				label {
							label "built-in"
							customWorkspace "/mnt/projects"
				
				}
		}
		
		environment {
						
						url = "https://github.com/mohanwaje/game-of-life.git"
		
		}
		
		stages {
		
				stage ("ClONE_PROJECT"){
								
							steps {
										sh "rm -rf *"
										sh "git clone $url"
							
							}
				
				}
				
				stage ("BUILD_PROJECT") {
							
								steps {
											
											sh "mvn clean install -DskipTests=true"
								
								}
				
				}
				
				stage ("COPY") {
							
							steps {
										sh "cp -r game-of-life/gameoflife-web/target/gameoflife.war /mnt/projects"
							
							}
				
				
				}
		
		
		
		}

}
