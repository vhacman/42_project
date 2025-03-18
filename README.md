1. **libft**  
2. **ft_printf**  
3. **get_next_line (GNL)**  
4. **Born2beroot**

Lo stile e l’impostazione rispecchiano le altre sezioni esistenti; nella tabella iniziale puoi aggiungere il tuo nuovo progetto GNL con relativo stato e punteggio (se già completato). Puoi ovviamente **personalizzare** date, punteggi e dettagli secondo necessità.

---

# 42 Roma Portfolio - Common Core
![42 Roma Badge](https://img.shields.io/badge/42-Roma_Luiss-2BA5DE)
![Profile](https://img.shields.io/badge/Profile-vhacman-orange)
![Status](https://img.shields.io/badge/Status-In_Progress-success)

## 🎯 Projects Overview

| Project                            | Description                       | Score                                                | Status | Completion    |
|------------------------------------|-----------------------------------|------------------------------------------------------|--------|--------------|
| [libft](#-libft)                   | C Standard Library Recreation     | ![Score](https://img.shields.io/badge/Score-100%2F100-brightgreen) | ✅      | January 2025 |
| [ft_printf](#-ft_printf)           | Printf Function Implementation    | ![Score](https://img.shields.io/badge/Score-100%2F100-brightgreen) | ✅      | February 2025 |
| [get_next_line](#-get-next-line-gnl) | Read File Descriptors by Lines    | ![Score](https://img.shields.io/badge/Score-125%2F100-brightgreen) | ✅      | March 2025   |
| [Born2beroot](#%EF%B8%8F-born2beroot) | System Administration             | ![Score](https://img.shields.io/badge/Score-110%2F100-brightgreen)     |✅      | February 2025 |

---

# 💯🎯 libft 🎯💯

## 📝 Description
The foundational project at 42 School, reimplementing essential C standard library functions and additional utilities used throughout the curriculum.

### 🛠️ Function Categories

#### 1️⃣ Libc Functions
| Function | Description | Complexity |
|----------|-------------|------------|
| ft_atoi     | ASCII to integer conversion        | O(n)   |
| ft_bzero    | Zero a byte string                | O(n)   |
| ft_calloc   | Allocate and zero memory          | O(n)   |
| ft_isalnum  | Test for alphanumeric character   | O(1)   |
| ft_isalpha  | Test for alphabetic character     | O(1)   |
| ft_isascii  | Test for ASCII character          | O(1)   |
| ft_isdigit  | Test for decimal digit            | O(1)   |
| ft_isprint  | Test for printable character      | O(1)   |
| ft_memchr   | Scan memory for a character       | O(n)   |
| ft_memcmp   | Compare memory areas              | O(n)   |
| ft_memcpy   | Copy memory area                  | O(n)   |
| ft_memmove  | Copy memory with overlap handling | O(n)   |
| ft_memset   | Fill memory with constant byte    | O(n)   |
| ft_strchr   | Locate character in string        | O(n)   |
| ft_strdup   | Duplicate string                  | O(n)   |
| ft_strlen   | Calculate string length           | O(n)   |
| ft_strncmp  | Compare two strings               | O(n)   |
| ft_strnstr  | Locate substring in string        | O(n*m) |
| ft_strrchr  | Locate character from end         | O(n)   |
| ft_tolower  | Convert to lowercase             | O(1)   |
| ft_toupper  | Convert to uppercase             | O(1)   |

#### 2️⃣ Additional Functions
| Function       | Description                    | Complexity |
|----------------|--------------------------------|------------|
| ft_itoa        | Integer to ASCII conversion    | O(log n)   |
| ft_putchar_fd  | Output character to fd         | O(1)       |
| ft_putstr_fd   | Output string to fd            | O(n)       |
| ft_putnbr_fd   | Output integer to fd           | O(log n)   |
| ft_split       | Split string using delimiter   | O(n*m)     |
| ft_strjoin     | Concatenate strings            | O(n+m)     |
| ft_strmapi     | Map function to string         | O(n)       |
| ft_strtrim     | Trim string ends               | O(n)       |
| ft_substr      | Extract substring              | O(n)       |

### 💻 Usage Example
```c
#include "libft.h"

int main(void)
{
    char *str = "42 Roma";
    
    // String manipulation
    size_t len = ft_strlen(str);
    char *dup = ft_strdup(str);
    
    // Character checks
    if (ft_isalpha('A'))
        ft_putchar_fd('A', 1);
    
    // Memory operations
    char *mem = ft_calloc(10, sizeof(char));
    ft_memset(mem, 'x', 9);
    
    // Cleanup
    free(dup);
    free(mem);
    
    return (0);
}
```

---

# ✨ ft_printf ✨

## 📝 Description
A custom implementation of the printf function, supporting various format specifiers and maintaining the efficiency of the original.

### 📊 Format Specifiers

| Specifier | Type      | Example                | Output |
|-----------|-----------|------------------------|--------|
| %c        | Character | `ft_printf("%c", 'A')` | A      |
| %s        | String    | `ft_printf("%s", "42")`| 42     |
| %p        | Pointer   | `ft_printf("%p", ptr)` | 0x7fff5694 |
| %d        | Decimal   | `ft_printf("%d", 42)`  | 42     |
| %i        | Integer   | `ft_printf("%i", -42)` | -42    |
| %u        | Unsigned  | `ft_printf("%u", 42)`  | 42     |
| %x        | Hex (lower) | `ft_printf("%x", 42)`| 2a     |
| %X        | Hex (upper) | `ft_printf("%X", 42)`| 2A     |
| %%        | Percent   | `ft_printf("%%")`      | %      |

### 🛠️ Implementation Structure
```c
// Core function
int ft_printf(const char *format, ...);

// Helper functions
int ft_putchar(char c);
int ft_putstr(char *str);
int ft_putnbr(int n);
int ft_putnbr_unsigned(unsigned int n);
int ft_putptr(void *ptr);
int ft_putnbr_hex(unsigned int n, char format);
```

---

# ♻️ get_next_line (GNL)

## 📝 Description
**get_next_line** è un progetto 42 che permette di leggere contenuti da un file descriptor una riga alla volta. Ora è incluso nella stessa libreria statica (`libft.a`), insieme a **ft_printf** e alle funzioni base di libft.  
Supporta sia la **versione base** che la **versione bonus** (lettura simultanea da più file descriptor).

### 🛠️ Main Features
- Lettura **line-by-line** con gestione del newline
- **BUFFER_SIZE** configurabile (macro)
- Memoria gestita con attenzione per evitare leak
- **Versione bonus**: lettura concorrente da più FD (fino a `OPEN_MAX`)

### 🔄 Workflow
1. Legge dati dal FD in blocchi (buffer)
2. Accumula il contenuto in una variabile statica
3. Restituisce la **prima riga completa** trovata
4. Conserva il “residuo” per la chiamata successiva
5. In caso di EOF o errore, ritorna `NULL`

### 🌐 Bonus
- `get_next_line_bonus.c` e `get_next_line_utils_bonus.c` usano un array statico di buffer per gestire in parallelo più descrittori.

### 💻 Example Usage
```c
#include "get_next_line.h"
#include <fcntl.h>
#include <stdio.h>

int main(void)
{
    int     fd;
    char    *line;
    
    fd = open("testo.txt", O_RDONLY);
    if (fd == -1)
    {
        printf("Errore nell'apertura del file\n");
        return (1);
    }
    
    line = get_next_line(fd);
    while (line != NULL)
    {
        printf("%s", line);
        free(line);
        line = get_next_line(fd);
    }
    
    close(fd);
    return (0);
}
```

### 🏆 Tips & Testing
- Prova `BUFFER_SIZE` piccoli (es. 1, 2) e grandi
- Testa file senza newline o file vuoti
- In bonus, apri più file (fd1, fd2, fd3…) e leggi in ordine alternato

---

# 🖥️ Born2beroot 🛡️

## 📝 Description
A system administration project focused on virtualization, Linux system management, and security implementation.

### 🔐 Security Features

#### Password Policy
```plaintext
Minimum length: 10 characters
Must contain: uppercase, lowercase, numbers
Maximum consecutive identical chars: 3
Cannot contain username
Must differ by 7+ chars from previous password
Expires after: 30 days
Minimum days between changes: 2
Warning period: 7 days
```

#### System Configuration
| Service | Configuration       | Port    |
|---------|---------------------|---------|
| SSH     | No root login       | 4242    |
| UFW     | Minimal ports       | Default deny |
| AppArmor| Enabled             | N/A     |
| Sudo    | Limited attempts    | N/A     |

### 📊 Monitoring Script
```bash
#!/bin/bash
# System information display
arch=$(uname -a)
pcpu=$(grep "physical id" /proc/cpuinfo | sort | uniq | wc -l)
vcpu=$(grep "^processor" /proc/cpuinfo | wc -l)
mem_use=$(free -m | awk 'NR==2{printf "%s/%sMB (%.2f%%)", $3,$2,$3*100/$2}')
disk_use=$(df -h | awk '$NF=="/"{printf "%d/%dGB (%s)", $3,$2,$5}')
cpu_load=$(top -bn1 | grep load | awk '{printf "%.1f%%", $(NF-2)}')
last_boot=$(who -b | awk '$1=="system" {print $3 " " $4}')
lvm_use=$(if [ $(lsblk | grep "lvm" | wc -l) -eq 0 ]; then echo no; else echo yes; fi)
tcp_conn=$(ss -ta | grep ESTAB | wc -l)
user_log=$(users | wc -w)
ip=$(hostname -I)
mac=$(ip link show | grep "link/ether" | awk '{print $2}')
sudo_cmd=$(journalctl _COMM=sudo | grep COMMAND | wc -l)

wall "
    Architecture: $arch
    CPU physical: $pcpu
    vCPU: $vcpu
    Memory Usage: $mem_use
    Disk Usage: $disk_use
    CPU load: $cpu_load
    Last boot: $last_boot
    LVM use: $lvm_use
    TCP Connections: $tcp_conn
    User log: $user_log
    Network: IP $ip ($mac)
    Sudo: $sudo_cmd cmd
"
```

## 📚 Study Resources
- System Administration Guide
- Security Implementation Guide
- Command Reference
- Defence Preparation Guide

---

## 👤 Author
**vhacman**  
- 42 Intra Profile: [vhacman](https://profile.intra.42.fr/)  
- Github: [@vhacman](https://github.com/DevGabi98)


## 📄 License
These projects are part of the 42 School curriculum. For usage and distribution, please refer to 42 School guidelines.
