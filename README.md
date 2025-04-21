# MAL-014: Authenticated Arbitrary File Read in VMware vCenter Server

The “com.vmware.appliance.version1.system.update.set” API component is vulnerable to a flag injection attack that can be leveraged with the “com.vmware.showlog” plugin in order to read arbitrary files as the “root” user on the target system.

**Note:** This vulnerability requires both admin access to the vCenter SSH shell as well as access to the filesystem as a low privilege user in order to create symlink files and/or folders.

### Collaboration:
This vulnerability was found in collaboration with Alexandru Bogdan.

### Requirements:

This vulnerability requires:
<br/>
- Valid credentials for user with "admin" role on the restricted vCenter SSH shell
- Access to the file system in order to create symlinks

### Proof Of Concept:

More details and the exploitation process can be found in this [PDF](https://github.com/mbadanoiu/MAL-014/blob/main/VMWare%20vCenter%20-%20MAL-014.pdf).

### Timeline:

- Vulnerability was reported to security@vmware.com (now vmware.psirt@broadcom.com) on 12-Apr-2023
- It was determined that the vulnerability could not be replicated in latest vCenter version at the time (8.0 U1)
- Publicly disclosed the vulnerability on 21-Apr-2025
