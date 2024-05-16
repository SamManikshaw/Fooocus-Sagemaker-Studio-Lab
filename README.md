# Fooocus-Sagemaker-Studio-Lab
Fooocus installer for [Sagemaker Studio Lab](https://studiolab.sagemaker.aws)

Simply add this repo to Sagemaker and run `sh start.sh`

How-to video:  
<a href="https://youtu.be/lzBlCA-QWdA"><img src="https://i3.ytimg.com/vi/lzBlCA-QWdA/maxresdefault.jpg" width=500) /></a>

### Installing in permanent storage
The app gets installed in temporary storage and is reinstalled each time the Sagemaker instance is restarted. To install the app in permanent storage, make sure to have at least 7.4 GB free space and edit the file `start.sh` to set the variable `install_in_temp_dir` to `false` in line 4.

Tutorial for models and storage manamgement: https://youtu.be/wFtj_JUxfWo  

---
### Updates
15/5/2024: Added support for Pinggy and Zrok - https://youtu.be/Tl5eHI_AMmw   

---
### Troubleshooting

#### I want to change the tunnel or another parameter I selected during installation.

Run
```
sh start.sh reset
```

#### OpenSSH fails to install.  

There is an error in the ouput saying "An unexpected error has occurred. Conda has prepared the above report."  
This is probably caused by a corrupted file in cache. To solve this problem, run
```
conda clean --all
```

#### Zrok fails to create a link.  

This is usually caused by an invalid token. You can generate a new token on your Zrok account page. To disable the existing token, open a terminal and run
```
zrok disable
```
You can enable the new token from the command line by running 
```
zrok enable PASTE_YOUR_TOKEN_HERE
```
To enable the token by using `start.sh`, start the app with 
```
sh start.sh reset
```
which will allow you to enter your new parameters. Alternatively, you can replace the old token in `data.json` and set `zrok_activated` to 0, to re-activate it with the new token.

---
### Fooocus on GitHub
Fooocus main repository: https://github.com/lllyasviel/Fooocus

---
Let’s connect!🌍
⭐ https://pogscafe.bio.link
