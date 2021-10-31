### To edit the website
#### Step 0: Clone repo and install necessary packages
*Note: this is only done once.*   
1. On your local machine, use the terminal to navigate to wherever you want to store your local version of the website. Then:
```
apt-get update
apt-get upgrade
git clone https://github.com/evpitcel/evpitcel.github.io
```
This will update and upgrade your system, and then create a new folder on your device containing the latest version of the website. The new folder will be named `evpitcel.github.io`.   

2. Next, navigate to this new folder and install `bundler`
```
cd ~/evpitcel.github.io
sudo gem install bundler
bundle install
```
3. If you get an error "while installing commonmarker" you might need to install additional libraries (zlib and ruby-dev) and then attempt bundle installation again. For MAC users, visit https://sourabhbajaj.com/mac-setup/Ruby/README.html and follow the steps there. If you did not get any errors, skip this part.
 ```
sudo apt install zlib1g
sudo apt install ruby-dev
bundle install
```  
4. Now you can create a local version of the website:
```
bundle exec jekyll serve
```
If you go to the website `http://127.0.0.1:4000` in your browser, you will see a local version of the site.    

5. To make sure it's working, open `evpitcel.github.io/aboutus` using your favorite text editor and change YOUR NAME in line 5 to say something else. Save the file and refresh `http://127.0.0.1:4000/people/YOURNAME`. You should see the header of the page change.

#### Step 1: Pull repo
From now on, every time you want to edit the website you will first have to pull whatever changes other people have made. To do this, navigate to your local folder and pull:
```
cd ~/evpitcel.github.io
git pull
```
This command incorporates changes from the remote (online) repository into your (local) branch.

#### Step 2: Make changes
You may now add pages, edit your people page, add news posts, etc. See below sections for specifics on how to make these kinds of changes. If you want to make more structural changes to the website, please make your own branch to test things out. We can merge them later when the Katie agrees to the bigger changes.

#### Step 3: Preview locally
Use the command `bundle exec jekyll serve` and go to `http://127.0.0.1:4000` on your browser to view a local copy of the website. This allows you to see how your changes will look before making them public.

#### Step 4: Commit changes
To save the current state of your version of the website, add and commit your edits:   
`git add .` adds all changes in the folder   
`git add FILENAME.txt` adds all changes in a specific file   

Then commit the changes using `git commit -m "DESCRIBE CHANGES"` to commit changes and add a description of  the changes you made.

#### Step 5: Push changes
To make your changes to the actual, public website, push them to the remote repository using:   
 `git push origin master`

Now everyone can see them and the website will be publicly updated. If you get an error on this step, someone else may have pushed after you last pulled. To fix this, `git stash` your changes, and talk to Katie or Ian.

---
### To add a news post:
1. Create a new post by making a copy of `_posts/YYYY-MM-DD-TEMPLATE.md` in the `_posts` folder
2. Change the title (line 3)
3. Change the date (line 4), keeping it in YYYY-MM-DD format
4. Add an image (line 7, optional)
     - `IMAGE_PATH` is the path to the image (e.g., /images/griff.jpg)
     - `ALT_TEXT` is text that will show if the image doesn't load
     - `CAPTION_TEXT` is text that will show when mouse hovers over image
5. add text (line 11)
6. See other posts in the `_posts` folder for reference.


---   
If you have questions, contact Katie.
