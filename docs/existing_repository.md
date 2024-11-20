# Clone exisiting repository

**1. Clone Repository**

### **Steps:**
1. Open your any browser and navigate to github portal 

2. Select your repository click on the code option right side of your repository choose any one option HTTPS/ SSH/ Git cli then copy the command

3. Navigate to the directory where you want to clone your repository:
```bash
   git clone <remote-repository-URL>
```
4. Add a new file to you repository:
```bash
   git add filename 
   ```
- To add all files in the directory to the staging area, use:
```bash
   git add . 

   ```
5. Commit your changes
``` bash
git commit m "commit message"
```
6. Push your changes
``` bash
git push origin main
```