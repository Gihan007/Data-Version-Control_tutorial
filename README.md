```md
# Data Version Control (DVC) Tutorial

This tutorial is created to demonstrate how to use DVC for versioning data files. It covers essential concepts such as tracking dataset versions, managing ML experiments efficiently, and ensuring reproducibility in machine learning workflows.

## Steps to Set Up DVC with Git

1. **Create a Git repository** and clone it into your local folder.  
2. Inside the repository, create `mycode.py` in Visual Studio Code.  
3. Add a simple data file using **Pandas** and Python.  
4. Perform initial Git setup:  
   - `git add .`  
   - `git commit -m "Initial commit"`  
   - `git push`  

## Installing and Initializing DVC

5. Install DVC:  
   ```sh
   pip install dvc
   ```
6. Initialize DVC:  
   ```sh
   dvc init
   ```
   - This creates `.dvcignore` and `.dvc` files.

## Setting Up DVC Remote Storage

7. Create a directory named `s3`.  
8. Add a remote storage location:  
   ```sh
   dvc remote add myremote s3
   ```
9. Track the data folder:  
   ```sh
   dvc add data/
   ```
10. Since Git already tracks the `data` folder, remove it from Git tracking:  
    ```sh
    git rm -r --cached data
    ```

## Committing and Pushing Data with DVC

11. Set the default remote:  
    ```sh
    dvc remote default myremote
    ```
12. Commit and push data using DVC:  
    ```sh
    dvc commit
    dvc push
    ```
13. Commit and push changes to Git:  
    ```sh
    git add .
    git commit -m "Track data using DVC"
    git push
    ```

## Updating Data and Versioning with DVC

14. Make changes to `mycode.py`, such as adding new data.  
15. Check DVC status:  
    ```sh
    dvc status
    ```
16. Commit and push new data version:  
    ```sh
    dvc commit
    dvc push
    ```
17. Save changes in Git:  
    ```sh
    git add .
    git commit -m "Version 2 of data"
    git push
    ```

18. Repeat steps **14-17** for **V3** of the data.

## Retrieving Specific Data Versions

19. To retrieve an exact version of a data file from Git:  
    ```sh
    dvc pull
    ```

## Conclusion

By following these steps, you can efficiently use **DVC** to manage and version control your project’s **data files** separately from the code. This allows you to revert to any previous data version based on Git commits.
```
