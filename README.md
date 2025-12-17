# Some-valuable-Command-for-ubuntu
Install Skype, VS-Code, postbird, tweak, chrome, brave, and many more

# Install Mattermost
~~~
sudo snap install mattermost-desktop
~~~

# Install VS-Code
~~~
sudo snap install code --classic
~~~

# Install Antigravity
~~~
curl -fsSL https://us-central1-apt.pkg.dev/doc/repo-signing-key.gpg \
  | sudo gpg --dearmor -o /etc/apt/keyrings/antigravity-repo-key.gpg && echo "deb [signed-by=/etc/apt/keyrings/antigravity-repo-key.gpg] https://us-central1-apt.pkg.dev/projects/antigravity-auto-updater-dev/antigravity-debian main" \
  | sudo tee /etc/apt/sources.list.d/antigravity.list && sudo apt update
&& sudo apt install antigravity
~~~

# Install universe repository
~~~
sudo add-apt-repository universe
~~~

# Install gnome-tweaks
~~~
sudo apt install gnome-tweaks
~~~

# Open tweak
~~~
gnome-tweaks
~~~

# Install extension for gnome (Optional)
~~~
sudo apt install $(apt search gnome-shell-extension | grep ^gnome | cut -d / -f1)
~~~

# Install chrome
first check wget
~~~
wget --version
~~~
then
~~~
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
~~~
then
~~~
sudo dpkg -i google-chrome-stable_current_amd64.deb
~~~

# Install video player decoder if you have issue to play videos
~~~
sudo apt-get install ubuntu-restricted-extras
~~~
or
~~~
sudo apt-get install libavcodec58 libav-tools ffmpeg
~~~
then
~~~
sudo apt remove gstreamer1.0-vaapi
~~~

# For clear Cache
first check disk usage
~~~
journalctl --disk-usage
~~~
then
~~~
sudo journalctl --rotate
~~~
then clear cache
~~~
sudo journalctl --vacuum-time=2days
~~~

# Convert from docx file to pdf file
~~~
lowriter --convert-to pdf CV.docx
~~~

# Corvert from pdf file to png photo
~~~
pdftoppm CV.pdf CV -png
~~~
~~~
sudo apt autoremove && sudo apt autoclean
~~~
