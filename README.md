# LIGO DCC Provisioner COmanage Registry Plugin

  1. If someone is added to an organizational group, DCC should be alerted.
  2. If someone is removed from an organizational group, DCC should be alerted.

Whether we do a push from Comanage or pull from LDAP? 
  - The current KAGRA provisioing is brute force. 
  - Brute force for pnp for also. 
  -Any record in ldap, verify record in the LDAP. After  LDAP record is checked, two lists: not verified then deprovision. Verified then add back in. 
  - DCC and pnp are codependent. Any change from Comanage level, one for DCC and pnp. pnp has its own database but also uses part of DCC database.
  - Potential: Comanage publishes i.e. push plug in from Comanage. 
  - If we pull, need ldap. We can have local HA replica. We cannot have two ldap's in the LINUX system. WE cannot merge LIGO and KAGRA ldap? Caltech replica both replicates gw-astronomy and ldap.ligo.org. 
  - It is not merging of LDAP. But two different LDAP's. 


Problems:
- In DCC there is no difference between oGROUP and aGROUP. 
- Satosa attributes dont match with what we have in LDAP. 
- LIGO vs KAGRA employeeNumber collides modulo KL. Hence DCC/pnp adds 88 for KL currently (hacky way).
