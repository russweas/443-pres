# Windows Quicklook Tool (WQT)

Problem: there is a larger backlog of cases than forensics experts can solve cases.

Solutions:
- Train more experts
- Decrease amount of cases
- **Make the forensics process quicker**

WQT will integrate the most used tools/workflows into a UI

Process:
- Bit copy source
- Look at system profiles, logs, login/logout timestamps, deleted files, HDD partitions


Research shows ools with poor UI result in poor work

Windows Event Viewer = terrible UI...

Windows Registry Editor = also terrible UI...

PyCharm = better UI
- dark mode
- editable interface - as simple or complicated as you want


Tools to include in WQT:
- Login/Logout timeline
- Browser Search Summary
- System profile summary
- Password fetcher
- Partition chart
- Tools involving other key Windows log events

## Login/Logout Timeline

Useful for reconstructing past events

First iteration - made in MS Paint

Left side - tool selection drop down

main panel - chart
- lines / bars for when something is happening
- services, batch, remote login, lock screen, login from start

Time change detections: for example, user changed system time into the past. 
- people change time for video games (want it to be night), want to hide something by going into the past

