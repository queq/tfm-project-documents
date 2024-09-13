<h1>Contents</h1>

- [Feature selection](#feature-selection)
  - [Supervised learning](#supervised-learning)
  - [Unsupervised learning](#unsupervised-learning)
- [Feature selection details](#feature-selection-details)
  - [Reference 1](#reference-1)
    - [Lexical features](#lexical-features)
    - [External features](#external-features)
  - [Reference 2](#reference-2)
    - [Features](#features)
  - [Reference 3](#reference-3)
    - [Features](#features-1)
  - [Reference 4](#reference-4)
    - [Features](#features-2)
  - [Reference 5](#reference-5)

# Feature selection

## Supervised learning

> | #  |      Column name     |                        Feature name                         |  Data Type  |
> | -- | -------------------- | ----------------------------------------------------------- | ----------- |
> | 1  | `url_length`         | URL length in characters                                    |    `int`    |
> | 2  | `starts_with_ip`     | Is the base URL an IP address?                              |    `bool`   |
> | 3  | `url_entropy`        | URL/hostname entropy                                        |   `float`   |
> | 4  | `has_punycode`       | Does the URL contain at least one punycode character?       |    `bool`   |
> | 5  | `digit_letter_ratio` | Digit-letter character ratio in URL                         |   `float`   |
> | 6  | `dot_count`          | Count of occurrences of dot (`.`) inside URL                |    `int`    |
> | 7  | `at_count`           | Count of occurrences of dot (`@`) inside URL                |    `int`    |
> | 8  | `dash_count`         | Count of occurrences of dot (`-`) inside URL                |    `int`    |
> | 9  | `tld_count`          | Does the subdirectory in the URL contain top-level domains? |    `int`    |
> | 10 | `domain_has_digits`  | Does the domain (base URL) contain digits?                  |    `bool`   |
> | 11 | `subdomain_count`    | Count of subdomains featured in the base URL                |    `int`    |
> | 12 | `nan_char_entropy`   | Charactter entropy of NAN** characters inside the URL       |   `float`   |
> | 13 | `has_internal_links` | Does the URL subdirectory contain links?                    |    `bool`   |
> | 14 | `whois_data`*        | Domain WHOIS record                                         |    `bool`   |
> | 15 | `domain_age_days`    | Domain age in days, according to extracted WHOIS record     |   `float`   |

## Unsupervised learning

- URL-Tokenizer
- Word embedding of text content
- **Others TBD**

# Feature selection details

## Reference 1

> Adap, Vielka Angela V., Gabriel A. Castillo, Erskine Jerrell M. Delos Reyes, Edward B. Ronquillo, and Larry A. Vea. “Do Not Feed the Phish: Phishing Website Detection Using URL-Based Features.” In Proceedings of the 2023 5th World Symposium on Software Engineering, 135–41. WSSE ’23. New York, NY, USA: Association for Computing Machinery, 2023. https://doi.org/10.1145/3631991.3632011

### Lexical features

- URL length
- Having IP address
- URL/Hostname entropy
- Usage of punycode
- Digit-letter ratio
- Dot count
- @ count
- Dash count
- TLD in path
- Digits in domain

### External features

- Domain age
- Website traffic
- ~~Rankings (Alexa, PageRank, Majestic, Umbrella, etc.)~~ Not useful for non ranked URLs
- DNS Record

## Reference 2

> Cuzzocrea, Alfredo, Fabio Martinelli, and Francesco Mercaldo. “A Machine-Learning Framework for Supporting Intelligent Web-Phishing Detection and Analysis.” In Proceedings of the 23rd International Database Applications & Engineering Symposium, 1–3. IDEAS ’19. New York, NY, USA: Association for Computing Machinery, 2019. https://doi.org/10.1145/3331076.3331087

### Features

- URL length
- Having IP address
- Website traffic
- Domain age

## Reference 3

> Kim, Taeri, Noseong Park, Jiwon Hong, and Sang-Wook Kim. “Phishing URL Detection: A Network-Based Approach Robust to Evasion.” In Proceedings of the 2022 ACM SIGSAC Conference on Computer and Communications Security, 1769–82. CCS ’22. New York, NY, USA: Association for Computing Machinery, 2022. https://doi.org/10.1145/3548606.3560615.

### Features

- Digit/letter ratio
- TLD count in path
- Dash count
- Digits in domain
- Multiple subdomains

## Reference 4

> Aung, Eint Sandi, and Hayato Yamana. “URL-Based Phishing Detection Using the Entropy of Non-Alphanumeric Characters.” In Proceedings of the 21st International Conference on Information Integration and Web-Based Applications & Services, 385–92. iiWAS2019. New York, NY, USA: Association for Computing Machinery, 2020. https://doi.org/10.1145/3366030.3366064.

### Features

- NAN char entropy
- Dot count
- Having links inside URL
- Having redirects

## Reference 5

>