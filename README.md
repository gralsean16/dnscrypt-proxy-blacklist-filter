### A basic filter list designed for the blacklist mechanism in [DNSCryp-Proxy v2](https://github.com/jedisct1/dnscrypt-proxy).

![Twitter Follow](https://img.shields.io/twitter/follow/CKsTechNews?label=Follow%20CK%27s%20Tech%20News&style=social)
[![Discord](https://img.shields.io/badge/Discord-Join%20CKs%20Technology%20Discord%20Server-orange)](https://discord.me/chef-koch)
[![Telegram](https://img.shields.io/badge/Telegram-Join%20CK's%20Tech%20News%20Telegram-blue)](https://t.me/CKsTechNews)
[![license](https://img.shields.io/github/license/CHEF-KOCH/dnscrypt-proxy-blacklist-filter.svg)](https://github.com/CHEF-KOCH/dnscrypt-proxy-blacklist-filter/blob/master/license.txt)
[![repo size](https://img.shields.io/github/repo-size/CHEF-KOCH/dnscrypt-proxy-blacklist-filter.svg)](https://github.com/CHEF-KOCH/dnscrypt-proxy-blacklist-filter)


Project Goal
------------

1. I like to provide a clean regular expression filter-list to avoid downloading heavy domain based filter lists.
2. The list should not only limited to ads, however finding a good regexp for e.g. malware domains is difficult and the challenge. Some legit page like Malwarebytes might also getting blocked if you use *.malware as filter.
3. Fix every reported issue and improve the list as much as possible.

Normal domain based filter lists are big in size, needs to maintained regularly and consuming a lot of memory and space. DNS based blocking with regular expression is better because you can block thousands of domains with only one single line.


## Usage

1) Open your `dnscrypt-proxy.toml` file there you find the black/whitelist categories.
2) Go under "Pattern-based blocking (blacklists)", comment out `blacklist_file = 'blacklist.txt'`
3) Do the same method for "Pattern-based IP blocking (IP blacklists)" and comment out `blacklist_file = 'ip-blacklist.txt'`
4) Do the same for "Pattern-based whitelisting (blacklists bypass)", and comment out `whitelist_file = 'whitelist.txt'`


## Debug

To see what's blocked ensure you comment out (remove #) from the `log_file`.


## Acknowledgements and References
* [[Feature Request] Black-/Whitelist and IP based rules won't allow you to import external lists](https://github.com/jedisct1/dnscrypt-proxy/issues/428)
