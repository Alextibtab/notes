---
thm_path: Red Team Fundamentals
thm_room: https://tryhackme.com/room/redteamfundamentals
platform: THM
---
# Red Team Fundamentals

## Vulnerability Assessments
The simplest form of security assessment, and it's main objective is to identify as many vulnerabilities in as many systems in the network as possible. To this end, concessions may be made to meet this goal effectively. For example the attacker's machine may be allowlisted on the available security solutions to avoid interfering with the vulnerability discovery process. This makes sense because the objective is to look at every host on the network and evaluate it's security posture.

A vulnerability assessment focuses on scanning hosts for vulnerabilities so that security deficiencies can be identified and effective security measures can be deployed to protect the network. Most of the work is done with automated tools and performed by operators without requiring much technical knowledge.

## Penetration Tests
On top of scanning every single host for vulnerabilities, we often need to understand how they impact the network as a whole. Penetration tests add to vulnerability assessments by allowing pentesters to explore the impact of an attacker on the overall network.
- Attempt to exploit the vulnerabilities found on each system. This is important as sometimes a vulnerability might exist in a system but controls in place effectively prevent the exploitation
- Conduct post exploitation tasks on any compromised hosts allowing us to find if we can extract any helpful information from them or if we can pivot further into the network.
Penetration tests might start by scanning for vulnerabilities just as in a regular vulnerability assessment but provide further information on how an attacker could chain the found vulnerabilities to achieve specific goals.

## Advanced Persistent Threats and why Regular Pentesting is not Enough
While the conventional security engagements we have mentioned cover the finding of most technical vulnerabilities, there are limitations on such processes and the extent to which they can effectively prepare a company against a real attacker.
- **Penetration tests are LOUD**: Usually, pentesters won't put much effort into trying to go undetected. Unlike real attackers, they don't mind being easy to detect, as they have been contracted to find as many vulnerabilities as they can in as many hosts as possible
- **Non-technical attack vectors might be overlooked**: Attacks based on social engineering or physical intrusions are usually not included in what is tested.
- **Relaxation of security mechanisms**: While doing a regular penetration test some security mechanisms might be temporarily disabled or relaxed for the pentesting team  in favour of efficiency. While it might sound counter intuitive the pentesters have limited time to check the network and would rather focus on reviewing critical infrastructure rather than trying to bypass IDS/IPS

## Red Team Engagements
Red team engagements were designed to shift the focus from regular penetration tests into a process that allows us to clearly see the defensive team's capabilities at detecting and responding to a real threat actor. They don't replace traditional penetration tests, but complement them by focusing on detecting and response rather than prevention.

Red teaming is a term borrowed from the military exercises, a group would take the role of a red team to simulate attack techniques to test the reaction capabilities of a defending team, generally known as blue team.

Red team engagements consist of emulating a real threat actor's **Tactics, Techniques and Procedures (TTPs)** so that we can measure how well the blue team responds to them and ultimately improve any security controls in place.

Every red team engagement will start by defining clear goals often references as **crown jewels** or **flags** ranging from compromising a given critical host to stealing some sensitive information from the target. Usually, the blue team won't be informed of such an exercise to avoid introducing any biases in their analysis.

Red team engagements also consider other attack surfaces:
- **Technical Infrastructure**: red team will try to uncover technical vulnerabilities with a much higher emphasis on stealth and evasion.
- **Social Engineering**: Targeting people through phishing campaigns, phone calls or social media to trick them into revealing information that should be private.
- **Physical Intrusion**: Using technologies like lockpicking, RFID cloning, exploiting weaknesses in electronic access devices to restricted areas of facilities.

Depending on the resources available the red team exercise can be run in several ways:
- **Full Engagement**: Simulate an attackers full workflow from initial compromise until final goals have been achieved.
- **Assumed Breach**: Start by assuming the attacker has already gained access over some of the hosts and achieve goals from there. As an example the red team could receive some user creds to give them an initial foothold.
- **Table-top Exercise**: An over the table simulation where scenarios are discussed between the red and blue teams to evaluate how they would theoretically respond to certain threats.


### Team Definitions
| Team      | Definition                                                                                                                                                                                                                    | 
| --------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | 
| Red Cell  | A red cell is the component that makes up the offensive portion of a red team engagement that simulates a given target's strategic and tactical responses.                                                                    |     
| Blue Cell | The blue cell is the opposite side of red. It includes all the components defending a target network. The blue cell is typically comprised of blue team members, defenders, internal staff, and an organisation's management. |     
| White Cell          |  Serves as referee between red cell activities and blue cell responses during an engagement. Controls the engagement environment/network. Monitors adherence to the ROE. Coordinates activities required to achieve engagement goals. Correlates red cell activities with defensive actions. Ensures the engagement is conducted without bias to either side.                                                                                                                                                                                                                             |     


### Red Team Roles
| Role | Purpose |
| ---- | ------- |
| Red Team Lead | Plans and organises engagements at a high level—delegates, assistant lead, and operators engagement assignments. |
| Red Team Assistant Lead | Assists the team lead in overseeing engagement operations and operators. Can also assist in writing engagement plans and documentation if needed.|
|Red Team Operator |Executes assignments delegated by team leads. Interpret and analyse engagement plans from team leads. |

# TODO Cyber Kill Chain

thm_room: https://tryhackme.com/room/redteamfundamentals
tags: #THM #Red_Team_Path