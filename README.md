# oss-audit-24bcg10141

# OSS Audit -Mrigank, Roll: [24BCG10141], Slot: [A11]


**Chosen Software**: Apache HTTP Server (`httpd`/`apache2`)  
**License**: Apache 2.0  
**Why chosen**: Powers 30% of websites globally - perfect OSS example from approved list.[file:1]


## Script Descriptions & Linux Run Instructions


All scripts tested on **Ubuntu/Fedora Linux**. **Dependencies**: `bash` (pre-installed), standard utils (`uname`, `rpm`/`dpkg`, `du`, `grep`). No extra packages needed.


### 1. system_identity.sh


**Purpose**: Displays Linux distro, kernel, user, uptime (Script 1 requirement: variables, echo, command substitution).


**Step-by-step**:
chmod +x system_identity.sh # Make executable
bash system_identity.sh # Run script

text


**Expected output**: Formatted system info with student name/software.


### 2. package_inspector.sh

**Purpose**: Checks if Apache (`httpd`/`apache2`) installed, shows version/license, case statement description (Script 2: if-then-else, case, rpm/dpkg/grep).


**Step-by-step**:

chmod +x package_inspector.sh
bash package_inspector.sh # Auto-detects RPM/Debian package manager
**Expected output**: "httpd is installed" + version/license OR "NOT installed" + Apache philosophy note.


### 3. disk_auditor.sh

**Purpose**: Audits space/permissions for `/etc`, `/var/log`, `/home`, `/usr/bin`, `/tmp` (Script 3: for loop, df/ls/awk/cut).


**Step-by-step**:

chmod +x disk_auditor.sh
bash disk_auditor.sh # Scans 5 key directories

text


**Expected output**: Table showing each dir's permissions, owner, size (e.g., `/etc drwxr-xr-x root root 150M`).


### 4. loganalyzer.sh


**Purpose**: Counts keyword occurrences in log file using while-read loop (Script 4: while loop, if-then, args).


**Step-by-step**:

chmod +x loganalyzer.sh
bash loganalyzer.sh /var/log/messages ERROR # System log example

OR for Apache:
bash loganalyzer.sh /var/log/httpd/access_log ERROR # Apache access log

text

**Expected output**: `"Keyword 'ERROR' found X times in /var/log/messages"`.


### 5. manifesto_generator.sh

**Purpose**: Interactive OSS philosophy generator (Script 5: read input, string concat, file write).


**Step-by-step**:

chmod +x manifesto_generator.sh


bash manifesto_generator.sh # Follow interactive prompts

**Expected output**: `manifesto_ishanvi.txt` created + content displayed.



## Testing Environment

- **Ubuntu 22.04**: `sudo apt install apache2`
- 
- **Fedora/RHEL**: `sudo dnf install httpd`
- 
- All scripts **run without sudo** except Apache installation for Script 4 testing.
- 


## Screenshots

Includes command+output screenshots in your PDF report (Section 4 requirement):
1. Each script running successfully
2. `manifesto_*.txt` file content
3. Apache package info from Script 2

