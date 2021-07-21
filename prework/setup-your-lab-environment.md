# Setup Your Lab Environment

## Hardware
- Your primary computer (that you Zoom into class with) must meet minimum hardware specifications as outlined on the [course website](https://www.codefellows.org/courses/ops-201/foundations-of-computer-operations/){:target="_blank"} under “Laptop Requirements.”

## Software

### Personal Computer

On the personal computer that you'll be attending class with:
- Connected your computer to a high speed internet connection, preferably using Cat6 ethernet cabling for optimal reliability.
- Install [Zoom](https://zoom.us/){:target="_blank"}. Use the Settings menu to pepare your webcam and microphone for use in class.
- Install [Slack](https://slack.com/){:target="_blank"} and ensure you are logged into the class chat. If you need an invitation, contact your instructor.
- Install [WinRAR](https://www.rarlab.com/rar/winrar-x64-591.exe){:target="_blank"} or 7-ZIP to handle compressed archives.
- Install [Git Bash](https://git-scm.com/downloads){:target="_blank"}.
- Install [Visual Studio Code](https://code.visualstudio.com/){:target="_blank"}.
- Install [WinSCP](https://winscp.net/eng/index.php){:target="_blank"} if you are a Windows user. MacOS users will need to install an alternative SCP GUI application, as WinSCP is not compatible with macOS.
- If you are a macOS user, install [Microsoft Remote Desktop](https://apps.apple.com/us/app/microsoft-remote-desktop/id1295203466?mt=12){:target="_blank"} from the Apple Store. Windows users may disregard, as RDP comes preloaded.
- Install [Google Chrome](https://www.google.com/chrome/index.html){:target="_blank"} for use with the Remo virtual campus.
- If you tested into Ops 201, create a bootable Ubuntu Linux 20.10 Desktop USB flash drive.


### Lab Computer

The following instructions detail Ubuntu software setup operations performed in Ops 102. If you took Ops 102, disregard this section. The objective of Ops 102 was to introduce non-computer users to the basics of computer operations by standing up a Ubuntu Linux lab PC that will act as a dedication VirtualBox server for use during the overall Ops program moving forward.

On the lab kit PC that you received from Code Fellows:
- Plug the computer into the same network as your personal computer. Use cabled ethernet connectivity if possible; wireless connectivity introduces variables that may negatively impact performance.
- Install Ubuntu Linux OS using the bootable flash drive provided in your lab kit. Format the drive FAT32 for compatibility.
- Once Ubuntu is installed, log into the Desktop and open the Terminal.
- Now we're going to load an automated setup script to stand up the required software. Run the following:
  - `sudo apt update`
  - `sudo apt install git -y`
  - `mkdir ~/github`
  - `cd ~/github`
  - `git clone https://github.com/lee5378/labsetup.git`
  - `sudo bash labsetup.sh` then answer yes to all prommpts

  > The install script takes a significant amount of time to complete. Keep an eye on it in case it's waiting on you for a "yes" prompt, otherwise feel free to work on other things while it loads.

When you have finished the lab setup script, you'll have some basic software including VirtualBox and GNS3 that will be used throughout the Ops program.

#### Lab System Operations

Next up, we need to make the lab computer accessible remotely from our personal Zoom computer.

- Assign a reserved IP to the lab computer. This is done from the DHCP server your lab computer is plugged into. This is typically a home router/cable modem appliance. If you cannot assigned a reserved IP to your lab computer, that's OK but you'll need to periodically check the IP of it so that you can remote in to the correct IP address.
- Install OpenSSH Server on the lab computer. Test and confirm SSH connectivity from personal computer to lab computer.
- Practice how to shutdown and reboot the lab computer from SSH terminal.
- Install XRDP on the lab computer. If you're a Windows user, RDP is built into Windows 10. Test and confirm remote desktop connectivity from personal computer or lab computer. 
  - MacOS users will need to download the RDP app from the Apple Store, in order to use RDP to connect to the lab PC.
- Install WinSCP on your personal computer and practice connecting to the lab computer for file transfer purposes.

Once you can connect to the lab computer via SSH, RDP, SCP, and can create virtual machines in VirtualBox, you're all caught up.

#### Windows 10 VM

Your final task is to create a Windows 10 VM in VirtualBox on the Ubuntu PC.
- In Ubuntu, download the [Windows 10 ISO (4.79 GB)](https://www.icloud.com/iclouddrive/01azgWsJOfzZaBbAj-G3sLWTg#Windows10) and mount it on a new VM in VirtualBox. Alternatively, you may create your own Windows 10 ISO using the Windows Media Creation Tool if you are on a compatible system.
- Deploy a user profile via the Windows first-time setup wizard.

Once you have a Windows 10 VM deployed, you're all caught up with Ops 102 grads. If you are an Ops 102 grad, indicate in your submission doc that you have reviewed these requirements and your systems configuration meets them.

## Submission Instructions

1. Create a new blank Google Doc. Include above assignment submission text and images within this Google Doc.
1. Name the document according to your course code and assignment.
   - i.e. `seattle-ops-201d1: Reading 01` or `seattle-ops-201d1: Lab 04`.
1. Add your name & date at the top of the Google Doc.
1. Share your Google Doc so that "Anyone with the link can view".
1. Paste the link to your Google Doc in the discussion field below and share an observation from your experience in this lab including how long this lab took to complete.
