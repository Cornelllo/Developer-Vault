
IP: `52.74.85.83`
Username: `ubuntu`
Use CPI-VPN to remote and use putty (CPI VPN available up to 9pm only
Email sender: no-reply@cpi.com.ph

**PowerShell RGB properties**
R: 91 G: 160 B:160

**Show Linux details and versions using any of the following**
`lsb_release -a`
`hostnamectl
`cat /etc/os-release`

**SSH From Windows 10**
OpenSSH using PowerShell(Administrator) after [[Convert export ppk to OpenSSH]]
and run the following command where you export the file
`ssh -i C:\Users\PROMEGA\Desktop\OpenEdx\openedx-server-key ubuntu@52.74.85.83`

**Prerequisite**
`sudo apt install python3.12-venv`
`docker run hello-world` (make this runs without issue)
`groups ubuntu` (check if user ubuntu belongs to docker group)

**Create the Python Virtual Environment**(tutor commands only work in the virtual env):
`python3 -m venv ~/Open-edX/tutor-env`

**Activate the Virtual Environment**

```
source ~/Open-edX/tutor-env/bin/activate
```

**How to eactivate the Virtual Environment**
```
exit()
deactivate
```

**Install Tutor**
`pip install "tutor[full]"`

**Verify Tutor either of the two commands
```
which tutor
tutor --version
```

### Use **`tutor local launch`** to setup for Production:

- **`tutor local launch`** is designed to guide you through the initial **setup and configuration** process, which is essential for production environments.
- It automates the setup of key configurations like **domain name**, **admin credentials**, **HTTPS** (SSL certificates), **SMTP** (email settings), and more.
- It prepares all necessary services (like MySQL, MongoDB, Redis) and deploys Open edX using Docker containers.

If you choose No for production this should be the final output:
All services initialised.
The platform is now running and can be accessed at the following urls:

    http://local.edly.io
    http://studio.local.edly.io
    http://apps.local.edly.io

Test connection in the SSH'd Linux server via with `curl -I http://local.edly.io
or just run `docker ps` to confirm the docker containers are running.

**Edit the `hosts` File**: On your local machine, add entries to your **`/etc/hosts`** (Linux/macOS) or **`C:\Windows\System32\drivers\etc\hosts`** (Windows) file to map the domain names to your server’s IP address.
```
52.74.85.83 local.edly.io
52.74.85.83 studio.local.edly.io
52.74.85.83 apps.local.edly.io
```
You should be able to access the local URLs of the Open edX in your Linux server using your local machine's browser.

Create a super user admin account and begin creating courses or import one via CLI
`tutor local do createuser --staff --superuser admin promega@cpi.com.ph`

View the admin page at
https://studio.learn.cpi.com.ph/admin/

![[Pasted image 20241010100853.png]]

**Make a course invitation only so public users are not able to enroll**
`select the course > go to settings > advance settings > set invitation only to true`

**Students register and sign in here:**
https://learn.cpi.com.ph/

**Course content creators here:** (view course as staff)
https://studio.learn.cpi.com.ph/

**To view OpenEdx config via Tutor**
`cat "$(tutor config printroot)/config.yml"`

**To edit OpenEdx config via Tutor**
`vim "$(tutor config printroot)/config.yml"`

**To save config changes run these**
`tutor config save`
`tutor local restart`

