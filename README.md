To avoid typing password everytime you use sudo command.

Step to use

Step# 1. Download script sudo_pass to any of bin directory. If you do not have permission to copy files other than your home directory then create a bin directory under your home directory and copy it there.

Step# 2. Make sure that script has execute permission. i.e. chmod +x sudo_pass

Step# 3. Run "sudo_pass -s" to set password. This will store your password under your home directory ".config/sudoPass/myPass" file.

  # sudo_pass -s

Step# 4. Once password is stored, set envirnment variable "SUDO_ASKPASS" to sudo_pass script. i.e. if the script is copied to your home directory bin.
  
  # export SUDO_ASKPASS="$HOME/bin/sudo_pass" 

Step# 5. Set alias to sudo command to "sudo -A". i.e. 
  
  # alias sudo="sudo -A"

You are all set to use sudo command now without password.

If you want to clear stored password when your done using sudo command run sudo -c i.e.
  
  # sudo -c
  
  this will clear the stored file. You may also add this command to "logout" script so that evertime you logout it will clear the password.
