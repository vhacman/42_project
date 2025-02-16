# 42 Roma Projects Portfolio
![42 Badge](https://img.shields.io/badge/42-Rome-2BA5DE)
![Status](https://img.shields.io/badge/Status-Active-success)

## 👨‍💻 Project Overview

| Project | Score | Status | Completion Date |
|---------|--------|---------|----------------|
| [libft](#-libft) | ![Score](https://img.shields.io/badge/Score-100%2F100-brightgreen) | ✅ | January 2025 |
| [ft_printf](#-ft_printf) | ![Score](https://img.shields.io/badge/Score-100%2F100-brightgreen) | ✅ | February 2025 |

---

# 💯🎯 libft 🎯💯

## 📝 Project Description
libft is the foundational project at 42 School, where we recreate essential C standard library functions. This library serves as a building block for all future projects in the curriculum.

### 🔑 Key Achievements
- Implemented 23 standard C library functions
- Created 9 additional utility functions
- Developed with strict memory management
- Zero memory leaks
- Passed all Moulinette tests

### 🛠️ Function Categories

#### Standard Library Functions
| Category | Functions |
|----------|-----------|
| String Operations | `ft_strlen`, `ft_strchr`, `ft_strrchr`, `ft_strncmp`, `ft_strnstr`, `ft_strdup` |
| Memory Operations | `ft_memset`, `ft_bzero`, `ft_memcpy`, `ft_memmove`, `ft_memchr`, `ft_memcmp` |
| Character Operations | `ft_isalpha`, `ft_isdigit`, `ft_isalnum`, `ft_isascii`, `ft_isprint`, `ft_toupper`, `ft_tolower` |
| Conversion | `ft_atoi` |
| Memory Management | `ft_calloc` |

#### Additional Functions
| Category | Functions |
|----------|-----------|
| String Manipulation | `ft_substr`, `ft_strjoin`, `ft_strtrim`, `ft_split` |
| Number Conversion | `ft_itoa` |
| Output Functions | `ft_putchar_fd`, `ft_putstr_fd`, `ft_putendl_fd`, `ft_putnbr_fd` |

---

# ✨ ft_printf ✨

## 📝 Project Description
A custom implementation of the printf function, handling various format specifiers while maintaining the efficiency and flexibility of the original.

### 🎯 Project Objectives
- Recreate printf functionality
- Handle multiple format specifiers
- Implement variable argument handling
- Ensure memory efficiency
- Match original printf behavior

### 📊 Supported Format Specifiers

| Specifier | Description | Example |
|-----------|-------------|----------|
| %c | Character | `ft_printf("%c", 'A')` |
| %s | String | `ft_printf("%s", "Hello")` |
| %p | Pointer | `ft_printf("%p", ptr)` |
| %d | Decimal | `ft_printf("%d", 42)` |
| %i | Integer | `ft_printf("%i", -42)` |
| %u | Unsigned | `ft_printf("%u", 4294967295)` |
| %x | Hex (lowercase) | `ft_printf("%x", 255)` |
| %X | Hex (uppercase) | `ft_printf("%X", 255)` |
| %% | Percent sign | `ft_printf("%%")` |

### 🔧 Technical Implementation
```c
int ft_printf(const char *format, ...)
{
    va_list args;
    int count;
    
    va_start(args, format);
    count = handle_format(format, args);
    va_end(args);
    
    return (count);
}
```

## 🚀 Skills Demonstrated

### Technical Skills
- Advanced C Programming
- Memory Management
- Pointer Manipulation
- String Processing
- Makefile Usage
- Git Version Control

### Soft Skills
- Problem Solving
- Attention to Detail
- Documentation
- Time Management
- Project Planning

## 🔨 Development Tools
- Language: C
- Compiler: gcc
- Build System: Make
- Version Control: Git
- Testing: Unit Tests

## 👤 Author
**vhacman**
- 42 Intra Profile: [vhacman](https://profile.intra.42.fr/)
- Github: [@DevGabi98](https://github.com/DevGabi98)

## 📊 GitHub Statistics
![GitHub Stats](https://github-readme-stats.vercel.app/api?username=DevGabi98&show_icons=true&theme=radical)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=DevGabi98&layout=compact&theme=radical)

## 📄 License
These projects are part of the 42 School curriculum. For usage and distribution, please refer to 42 School guidelines.
