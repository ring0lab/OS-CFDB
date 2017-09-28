
# Finding Details 

## Title
  MsCacheV2 Misconfiguration 
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
  * https://technet.microsoft.com/en-us/library/jj852209.aspx
  * https://webstersprodigy.net/2014/02/03/mscash-hash-primer-for-pentesters/
  
# Technical Information

## Description 
MsCacheV2 is a Microsoft implementation of local password storage for domain users. These credentials are implemented using the registry and the local SAM hive. By default, Windows caches up to 10 credentials locally and removes the oldest credential as they populate to the host. Caching takes place for Interactive Logons (Type 2), Service Logon (Type 5), and Remote Interactive Logons (Type 10).

## Impact
If an attacker can gain elevated system privileges on a compromised host, the attacker could gather MsCacheV2 credentials. These hashes could then be potentially cracked using the PBKDF2 hashing algorithm, which uses the “Username” as the known salt value. Cracked MsCacheV2 credentials could potentially be used for further lateral movement or compromise of internal domain systems.  

## Recommendation(s)
The assessment team recommends that MsCacheV2 credential caching is limited to three accounts at any given time. This setting can be adjusted via GPO (Group Policy Objects).

# Finding Metadata
  * Author(s)
    * Alexander Rymdeko-Harvey (@Killswitch-GUI)
  * Source(s)
  * Created
    * 09/27/2017
  * Updated
    * 09/27/2017