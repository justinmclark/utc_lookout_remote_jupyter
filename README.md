# First things first
1. Get a user account with Ethan and set up a VPN so you can ssh onto the server remotely.
2. Learn a little bit about managing environments with Anaconda.

# Instructions
Connect to VPN so `ssh` works
```local> ssh <user>@lookout00``` (could be lookout01, 02, 03 as well)

```lookout> export PATH=/usr/local/anaconda2/bin:$PATH```

```lookout> conda create -n env_name python=3.5```

```lookout> source activate env_name```

If not installed already, install Jupyter
```(env_name) lookout> conda install jupyter```

