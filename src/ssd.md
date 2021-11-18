# Solid State Drives
Improved reliability, speed over HDD’s

Garbage collection process
Memory Cells -> Pages -> Rows -> Blocks

Over psvisioning – frequent writing to same cell makes it go bad
Over provisioning sector is makred for deleted data and is inaccessible in the future

GC makes forensics tough

Project: priority tree to predict las t blcoks of data accessed using probabilities
-	Need unrestricted access to FS
-	Use logs and metadata to generate predictions for files and map those files to SSD blocks
-	Will need access to NAND flash on the SSD, the Memory Controller would be an intermediary

Other problems: SSD’s can wipe all data in a few seconds. 
