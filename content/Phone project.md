## Rational
Our current system is the Mitel MiVoice 250. It's a fancy name, but it is old. Here are some dates
- Originally shipped around 2010
- End of life was January 2023
- End of technical support June 2026

What do those end of life dates mean? Well it basically means that in 2023 there were no more updates for:
- New features
- Bug fixes
- Security updates

The 2026 date means that no more service contracts could run or be issued for this system. That doesn't mean we cannot get service, we just have to pay for it one issue at a time. This can be expensive and think of it like a 15 year old car. There will be some repairs that just aren't worth performing because the cost of the repair will be worth more than the vehicle system itself. That's where we are at.

## Issues & how it works
Luckily we have not had any major issues with this system. It has pretty much been a tank and it still works
 ![[Zight 2026-05-22 at 10.28.49 AM.jpg|224]]

So we basically have three separate devices that all need work for the phone system to work. If the Mitel server goes down, the whole phone system goes down. If the voicemail fails, we obviously cannot access out VM and no one can leave new VMs.

If the User management server fails, the phone system will work as it was last modified, but no future modifications can be made. This server DID go down in April and for about a week we had no way to access the system. The server that housed the software failed and the redundancy did not work. :( 

We luckily had installed a brand new server the summer before and with the help of Gibson Teldata installed the software on that server, logged in and we had access again.

The lesson we learned here is that if the MItel server did go down - there would be no fixing that as we would need to get a replacement Mitel server (which aren't made anymore) and there is a boat load of work to do to set that thing up:
- Installation
- Configuration
- Setting up all phone lines again
- Configuring handsets to find new server

All this would take time and money and it is probably not worth it

## Choices
Luckily there have been big changes in this type of technology over the past 15 years. 

Our system is an **on-prem system**. That means that all the hardware is housed in our campus and it relies on [SIP Trunking](https://aws.amazon.com/what-is/sip-trunking/) from a local telecommunications company (Comcast, AT&T, etc.) Newer systems like this still exist but we would need newer equipment in order for it all to work.
- New VM server
- New server for the phone system itself

The other choice is a **cloud phone system**. This is just what it sounds like. The entire system is setup, managed and runs entirely on a server not in our building. 

There are pros and cons for each and let's go through them.

| On-prem     | Pro                                                                                                                                             | Con                                                                                                                                                                                                                                                                         |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Local       | We have access to all the hardware and control of everything.                                                                                   | Since it is local it is up to us to make sure it is up to date and any misconfiguration can cause disruptions                                                                                                                                                               |
| Setup       | Usually a one-time fee                                                                                                                          | Since we need actual devices set up, we would need to pay for the devices and their setup - it is costly                                                                                                                                                                    |
| Updates     | Updates are usually thoroughly tested before being available - meaning they won't cause much issues                                             | We have to perform the updates ourself. It's not hard, but may require a service agreement with the company. If something does go wrong we need to manually uninstall it. Since they control the cadence of what updates come out it takes longer to fix bugs in the system |
| Internet    | Since it is reliant on a phone company - if our Internet goes down, our phones will still work. We will be able to make and receive phone calls |                                                                                                                                                                                                                                                                             |
| Cost        | Once it is paid off, we are only paying for the trunking from the phone company                                                                 | The initial cost is substantial - upwards of $50,000 easily.                                                                                                                                                                                                                |
| Privacy     | Since everything is on our hardware, we have much more privacy                                                                                  |                                                                                                                                                                                                                                                                             |
| Access      |                                                                                                                                                 | Access to the system outside of the campus isn't an issue for most users, but for Technology it is not the easiest way to access while off campus                                                                                                                           |
| Longevity   | The system is built to last for more than a decade                                                                                              | The system will eventually run into an end of life date and leave us in the same predicament                                                                                                                                                                                |
| Ease of use | Pretty straightforward for end users                                                                                                            | Far more complicated for Technology to manage, but not unmanageable                                                                                                                                                                                                         |

The other option is a **Cloud phone system.** It is what you would think. Instead of the hardware housed on our campus, that hardware is housed in a secure data center somewhere in the US. Both will have similar features for end users but there are drastic differences in the system itself. Here are the pros/cons


| Cloud       | Pros                                                                                                                                                                                                                                                                                            | Cons                                                                                       |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| Local       | It's not here! The provider houses this and have their own redundancies in case our instance goes down                                                                                                                                                                                          | We give up some control of the system                                                      |
| Setup       | We really only setup the phones and have no real hardware to install or manage. We can have a cloud system up and running within a single day                                                                                                                                                   |                                                                                            |
| Updates     | More updates, more often and done automatically. It is one less thing to worry about. If an update fails, they are responsible for rolling it back. We will also get updates for as long as we have the service. There will be no end of life for the service unless to company fails to exist. | Since we don't manage them, if there are issues we are beholden to them to fix it.         |
| Internet    | These can integrate better with virtual meeting apps and can also integrate with third party apps like Google Calendar                                                                                                                                                                          | If the Internet goes down, our phones go down.                                             |
| Cost        | Much, much cheaper setup and installation fees and only pay to one place. We would have no need for a SIP Trunk with our local phone company.                                                                                                                                                   | We pay every month for the service. So over time it may prove to be                        |
| Privacy     |                                                                                                                                                                                                                                                                                                 | It runs on their server, so they have access to our VMs if they really wanted access to it |
| Access      | We can access it anywhere we have an Internet connection                                                                                                                                                                                                                                        | If no Internet, no phone :(                                                                |
| Longevity   | Since we are beholden to hardware or software that can be outdated, it will last much, much longer than an on-prem system                                                                                                                                                                       |                                                                                            |
| Ease of use | Just as easy for end users, but management is much, much easier.                                                                                                                                                                                                                                | We may lose some control since we don't have access to the entire hardware                 |

[[Phone features]]
[[Who gets access]]
[[Phone committee + Timeline]]
[[Demos]]
[[Laws to consider]]
[[What about Google Voice?]]