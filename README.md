# LIGO DCC Provisioner COmanage Registry Plugin

  1. If someone is added to an organizational group, DCC should be alerted.
  2. If someone is removed from an organizational group, DCC should be alerted.

Whether we do a push from Comanage or pull from LDAP? 
  - The current KAGRA provisioing is brute force. 
  - Brute force for pnp for also. 
  -Any record in ldap, verify record in the LDAP. After  LDAP record is checked, two lists: not verified then deprovision. Verified then add back in. 
  - DCC and pnp are codependent. Any change from Comanage level, one for DCC and pnp. pnp has its own database but also uses part of DCC database.
