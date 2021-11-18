# SSD Garbage Collection

SSD moves frequently used files around to fresher blocks to increase overall lifetime of SSD

Problems
- SSD with no file changes can change its hash
- Information location is not predictable

SSD gc 

TRIM (Delete Notification)
- Identifies pages as valid or invalid

```cmd
fsutil behavior query DisableDelteNotify
NTFS DisableDeleteNotify = 0 (Disabled)
ReFS DisableDeleteNotify = 0 (Disabled)
```

When disabled, active GC is disabled. File is only erased when its time to overwrrite the sector

Active GC called in background while device has power

No way to disable active GC without cutting off SSD power

## What can be done?

Disable TRIM

This severely harms SSD longevity and speed

Not selective - turning off TRIM turns it off for everything on the system

South Korea has the technology, but he couldn't translate it

## Selective TRIM Proposal

Adding additional conditions to TRIM flagging pages. Rather than invalid vs valid, four states:

Two "Reserved" States: Involuntary v Voluntary

### Reserved State

Data is deleted similiar to how it would be in a HDD

Data marked as reserved would be kept between GC runs, to be completely erased after 30 days

Preserves documents beyond initial GC run

Involuntary
- First page of file's data upon deletion

Voluntary
- Reserves entire file's data upon deletion

How would this aid forensics?

Having erased data survive on an SSD is a significant aid to attempt to recover data in investigations

Most people don't know they're being investigated more than a month in advance

