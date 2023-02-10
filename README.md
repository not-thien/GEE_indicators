# For GEE Use - Currently configured for Senegal

This file is the code for a web app that has multiple different indicators for degraded land. The study zone is the country of Senegal. 

*Note: The file `admin_EVI_avgs` has more than just EVI averages (I'm lazy to change it). It also has several imports that are necessary for the web app to run smoothly*

## How to Run:

**Option 1:** If you want to see the webapp, check out this [link](https://nguy3856.users.earthengine.app/view/senegal-evi-v02). 

**Option 2:** If you want to clone this repo and then push to your own GEE editor, it's a bit of an involved process. **Option 3** might be faster if you haven't done the following before:

1. In your browser, go to https://www.googlesource.com/new-password and copy the code generated into Git Bash to configure Git and authenticate to Earth Engine.

2. Add the Earth Engine repository you want to push this script into as a remote connection, replacing `USERNAME` and `REPOSITORY` with your GEE username and your repository, respectively:
> `git remote add ee https://earthengine.googlesource.com/users/USERNAME/REPOSITORY`

3. It is important that the local branch where your scripts are stored is named ‘master’, otherwise Earth Engine will not recognise the path. Run the following command to change the current branch name, replacing currentname with the name of your branch. [^1]
> `git branch -m currentname master`

4. Push the scripts from your local branch to the Earth Engine repository added as a remote connection earlier.
> `git push -u ee master`

**Option 3:** Simply copy and paste the code in `admin_EVI_args` and then convert the import variables when you are editing on the GEE code editor. Sometimes the easy way is the best :)

[^1]: One thing to note is that Git is not able to parse folders within an Earth Engine repository, so ensure that all your scripts are in the root repository and that there are no folders in there before attempting to clone the repository.