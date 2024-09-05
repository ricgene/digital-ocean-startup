So the thing with DO is, they still charge you if the droplet isn't running. So I've been deleting them when I'm done and then re-running all the setup commands (Docker install basically) when I start a new one.

I've uploaded the commands into a private repo and added you to it, here: awilliamso6/digital-ocean-startup: Info on how to set up a DO droplet from scratch (github.com) 
You can log in via root initially via SSH and run root_commands.txt, then you'll have a sudo user that you can log in with to run user_commands.txt

After that you can clone the climate-oracle repo. Then one more step, for the NOAA API you need a token, so you need to create a .env file in the climate-oracle base directory and put the NOAA_TOKEN value inside that. I didn't want to put that in the public repo of course.

After that I just run this in the base directory:

docker compose up -d --build

So theoretically you should be able to do all these same steps on a GCP instance.
(by Andrew W)
