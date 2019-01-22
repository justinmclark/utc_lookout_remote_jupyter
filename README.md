# First things first
1. Get a user account with Ethan and set up a VPN so you can ssh onto the server remotely.
2. Learn a little bit about managing environments with Anaconda.

# Instructions
Connect to GlobalProtectVPN so `ssh` works.

```local> ssh <user>@lookout00``` (could be lookout01, 02, 03 as well)

```lookout> export PATH=/usr/local/anaconda2/bin:$PATH```

```lookout> conda create env_name```

```lookout> source activate env_name```

If not installed already, install Jupyter (and anything else you need - like scipy, tensorflow, keras, etc.)

```(env_name) lookout> conda install jupyter```

Set a password for your personal Jupyter usage (make it a good but memorable one).

```(env_name) lookout> jupyter notebook password```

Run a headless version of Jupyter Lab instance. This will expose Jupyter on port 9000 of the lookout instance you're `ssh`ed into.

```(env_name) lookout> jupyter notebook --port=9000 --no-browser &```

```local> ssh -N -f -L localhost:8888:localhost:9000 <user>@lookout00``` (again, could be lookout01, 02, 03)

Now, just open up `localhost:8888` in your browser and you'll have have a Jupyter Notebook running from the lookout servers.
