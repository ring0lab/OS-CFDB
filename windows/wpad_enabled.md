
# Finding Details 

## Title
  WPAD Enabled 
## SVR
  4
## CVSS
  6.0 – 7.9
## Risk
  High
## Service
  * Internal Penetration Testing
  * External Penetration Testing 
## NIST 800-53 
  * CM-2
  * CM-6
  * IA-2
  * IA-3
## Refrences
  * https://www.trustedsec.com/2013/07/wpad-man-in-the-middle-clear-text-passwords/
  * https://technet.microsoft.com/en-us/library/security/ms16-077.aspx
 
# Technical Information

## Description 
WPAD (Web Proxy Auto-Discovery Protocol) affects any system that has "Auto Discovery Proxy Settings" turned on, this is default behavior within Windows. WPAD can often be used in environments but can present an attack surface if a host is compromised, or allow an attacker to gain access to an internal LAN (Local Area Network).

## Impact
Leaving WPAD enabled could allow an attacker using host or network-based toolsets to gather clear-text credentials over the network. These attacks can lead to SMB or HTTP relay attacks of NTLM credentials and code execution in certain conditions. In certain cases, this attack can allow an attacker to also perform privilege escalation from a normal local/domain user. 


## Recommendation(s)
The assessment team recommends following security best practices, by completely disabling WPAD. Windows has, however, a per-user and per-system proxy settings. Remediated with login scripts, GPO settings and registry edits can significantly increase the security of the network.

# Finding Metadata
  * Author(s)
    * Alexander Rymdeko-Harvey (@Killswitch-GUI)
  * Source(s)
    * https://github.com/mubix/cfdb/blob/master/Windows/WPAD.md
  * Created
    * 09/27/2017
  * Updated
    * 09/27/2017