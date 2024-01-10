# SOC Use cases
(NOTE: some of the entries are based on a document downloaded from linkedin)
## What are use cases?
The use cases are critical to identifying any of the early, middle, and end-stage operations of
the adversary. A small abnormal event can be a clue to a larger attack. There also needs to 
be a playbook on how to respond. A use case can be technical rules or conditions applied on 
logs which are ingested into the SIEM. E.g. – malicious traffic is seen hitting critical servers of 
the infra, too many logins attempt in last 1 min etc.

## Best practises
1. Ensure to have a clear list of your use cases handy always.
2. The use cases need to be mapped to the MITRE ATT&CK phases so you can know how 
much the adversary succeeded in his objective. Tagging and mapping to the MITRE
ATT&CK Matrix would help detection (what logs to be tapped into) and mitigation. Also 
helps attribution to an APT group.
3. Each use case to have a clear priority based on your organisation.
4. Each use case to have the log source which must be ingested into your SIEM.
Why it is important to have a large set of use cases and have playbooks for them? 
1. Real cyber-attacks are complex. It is actually very hard for the attacker to be invisible to a
SOC who has enabled the right set of use cases.
2. Use cases are rules that trigger alerts. You need playbooks or instruction on how to 
respond to them, steps to analyse and mitigate.
3. The process of creation of playbooks is very important. It helps a lot for you to be 
prepared for handling a cyber-attack. 


> NOTE: I attached the complete use cases in this directory for your reference. 