## Jim Harris - 05 JAN 2022 - Cycode Technical Assignment

#### Create an output.md file capturing the steps you followed to run the application and the screenshot of the homepage.

    sudo apt-get install git
    mkdir -p /path/to
    git clone https://github.com/jharrisDeFy/robot-shop.git
    cd /path/to/robot-shop
    sudo apt-get install docker-compose
    docker-compose build
    docker-compose up
    
![screen01_initial](https://user-images.githubusercontent.com/85969609/148298646-211c8210-4a3f-4fb2-b65f-bc2074575d17.GIF)

#### Is there anything wrong with committing the file directly to the master branch? 

 - Typically you want to make development changes to a development branch separate from the master branch.  The master branch should be reserved for code that is tested to be within the parameters for security and functionality defined for the project.  Master branches are often considered the gold standard to be used for CI/CD build and deliverables.  Once code is tested for quality and accepted by project leadership, then it can be requested to be merged into the master branch.

#### How would you prevent that?

 - By creating or using an existing development branch seperate from the master branch.  Once testing is complete and the code in the development branch has been approved, a request can be made to the administrator(s) of the master branch to merge the new code into the master branch.

#### Find a fun, cool logo to replace the current one on the main page. Also put a signature at the bottom. Merge your changes into the main branch of your repo and add a screenshot of the new main page to output.md

    vim ./web/static/index.html
    git commit -a -m "Edited static index.html file to include signature at the bottom of the page, and merging directly to master branch"
    git push
    docker-compose build
    docker-compose up
    
![screen02_edited](https://user-images.githubusercontent.com/85969609/148299502-3b922c99-d9a4-46c2-b3aa-a8d927072681.GIF)
