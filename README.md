# Data-Version-Control_tutorial
hey this is my Data versioning control tutorial , which is done by Gihan lakmal. 

create Git repo and clone it into Local folder.
then created mycode.py inside the visual then added simple Data file , which used panadas and python.
do the  git , add , commit and push before start DVC
#pip install DVCnow we do "DVC INIT" (CREATES .dvcignore4 .dvc)
now we make "director called S3" 
now create "dvc remote add myremote s3"
ad "dvc add data/"
since already git tracking the data folder , lets remove now it from tracking by the git
make dvc remote default  use ing "dvc remote default myremote"
now use dvc commit and dvc push
now do git -add -commmit -push to make commit the first version of current copy
now we doning changes to mycode.py , like adding new datas and stuff , then lets check how was the dvc status

 Again - - "dvc commit" and then "dvc push"
 Then git add-commit-push (we're saving V2 of our data at this point)
 Check dvc/git status, everything should be up to date.
 Now repeat step 10-12 for v3 of data.

 In this nway u can use DVC contolling for ur projects and maintain dta sheets and data files sepetaly. 
 based on the Commited version on the git , u can get into the exact data sheet at that time useing "dsv pull" commond.
