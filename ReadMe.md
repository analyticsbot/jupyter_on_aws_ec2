# download location is documents for me, you can choose accordingly
neo@neo:~/$ cd Documents/

# download repos to folder named github
neo@neo:~/$ mkdir github

# change director
neo@neo:~/Documents/$ cd github/

# install curl
neo@neo:~/Documents/github$ sudo apt install curl

#install git
neo@neo:~/Documents/github$ sudo apt install git

# download the repos using curl
neo@neo:~/Documents/github$ curl -s https://api.github.com/users/analyticsbot/repos?per_page=200 | grep \"clone_url\" | awk '{print $2}' | sed -e 's/"//g' -e 's/,//g' | xargs -n1 git clone

I've shared the steps in this video as well. 

Video location - https://youtu.be/0wr9MzwAdpY

Inspired from - https://gist.github.com/milanboers/f34cdfc3e1ad9ba02ee8e44dae8e093f
