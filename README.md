# 42 Roma Projects Portfolio
![42 Badge](https://img.shields.io/badge/42-Rome-2BA5DE)
![Status](https://img.shields.io/badge/Status-Active-success)

## 👨‍💻 Project Overview

| Project | Score | Status | Completion Date |
|---------|--------|---------|----------------|
| [libft](#-libft) | ![Score](https://img.shields.io/badge/Score-100%2F100-brightgreen) | ✅ | January 2025 |
| [ft_printf](#-ft_printf) | ![Score](https://img.shields.io/badge/Score-100%2F100-brightgreen) | ✅ | February 2025 |
| [Born2beroot](#-born2beroot) | ![Score](https://img.shields.io/badge/Score-In_Progress-yellow) | 🔄 | February 2025 |

---

[Previous projects content remains the same until Born2beroot section]

---

# 🖥️ Born2beroot 🛡️

## 📝 Project Description
Born2beroot is an immersive system administration project that focuses on the fundamentals of virtualization, Linux system management, and security implementation. The project involves creating and configuring a virtual machine with specific security requirements.

### 🎯 Project Objectives
- Create and configure a Virtual Machine
- Implement strict security policies
- Set up system monitoring
- Configure basic web services
- Learn system administration fundamentals

### 🔑 Key Components

#### Virtual Machine Setup
```bash
# Check system version
uname -a

# View disk partitions
lsblk

# Check UFW status
sudo ufw status

# Monitor system
./monitoring.sh
```

#### Security Implementation
| Feature | Description | Configuration |
|---------|-------------|---------------|
| Password Policy | Strong password requirements | `/etc/pam.d/common-password` |
| UFW | Firewall configuration | Port 4242 for SSH |
| SSH | Secure remote access | No root login allowed |
| AppArmor | Mandatory access control | Enabled by default |
| Sudo | Enhanced security rules | Custom configuration |

#### System Monitoring Script Features
- Architecture information
- CPU physical/virtual processors
- Memory usage
- Disk utilization
- CPU load
- Last boot time
- LVM status
- Active connections
- User log
- Network status
- Sudo commands log

### 📊 Technical Specifications

#### Password Requirements
```plaintext
- Minimum length: 10 characters
- Must contain: uppercase, lowercase, numbers
- Max 3 consecutive identical characters
- Cannot contain username
- 7 characters different from previous password
- Expiration: 30 days
- Minimum days between changes: 2
- Warning: 7 days before expiration
```

#### Service Configuration
- SSH running on port 4242
- UFW configured with necessary rules
- Monitoring script scheduled via crontab
- Optional: WordPress with Lighttpd, MariaDB, PHP

### 🛠️ Implementation Details
```bash
# Check SSH status
sudo systemctl status ssh

# View UFW rules
sudo ufw status verbose

# Monitor cron jobs
sudo crontab -l

# View system logs
sudo journalctl
```

## 📚 Study Resources
- [System Administration Guide](Prima_Parte.pdf)
- [Security Implementation](Parte_Seconda.pdf)
- [Defence Preparation](Preparazione_Defence.pdf)
- [Command Reference](Tabella_Comandi.pdf)

## 🎓 Learning Outcomes
1. System Administration
   - Linux system management
   - Service configuration
   - User and group administration

2. Security
   - Firewall configuration
   - Access control
   - Password policies
   - System hardening

3. Virtualization
   - VM creation and management
   - Resource allocation
   - Disk partitioning

4. Monitoring
   - System metrics
   - Resource usage
   - Service status
   - Log management

## 👤 Author
**vhacman**
- 42 Intra Profile: [vhacman](https://profile.intra.42.fr/)
- Github: [@DevGabi98](https://github.com/DevGabi98)

## 📊 GitHub Statistics
![GitHub Stats](https://github-readme-stats.vercel.app/api?username=DevGabi98&show_icons=true&theme=radical)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=DevGabi98&layout=compact&theme=radical)

## 📄 License
These projects are part of the 42 School curriculum. For usage and distribution, please refer to 42 School guidelines.