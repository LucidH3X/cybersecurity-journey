# OverTheWire Bandit Progress

**Started:** October 19, 2025  
**URL:** https://overthewire.org/wargames/bandit/

## Progress Tracker

- [x] Level 0 → 1: Basic `cat` command
- [x] Level 1 → 2: Files with special names (`-`)
- [x] Level 2 → 3: Files with spaces in name
- [ ] Level 3 → 4: Hidden files
- [ ] Level 4 → 5: File types
- [ ] Level 5 → 6: Finding files
- [ ] Level 6 → 7: Finding files by owner
- [ ] Level 7 → 8: Grep command
- [ ] Level 8 → 9: Unique lines
- [ ] Level 9 → 10: Strings in binary
- [ ] Level 10 → 11: Base64

## Commands Learned

### Level 0-1
```bash
ls          # List files
cat [file]  # Read file contents
```
![[Pasted image 20251018151453.png]]
### Level 1-2
```bash
cat ./-     # Read files starting with dash
```
![[Pasted image 20251019114138.png]]
Flag: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx

- So on Level 1-2 I has some issues I ran into *-* for the first time. I have never seen this file type and when I ran `cat -` It froze up my shell. I had to pull open google to look into the issue and found that in cases that this pops up we need to run `cat ./-` to view the file so its specific otherwise it will search everything with *-* 
### Level 2-3
```bash
cat -- "--spaces in this filename--"  # Files with spaces
```
![[Pasted image 20251019120245.png]]
Flag: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
- So this one was weird I ran into issues using `cat --spaces in this filename-- ` because when it sees `--` it thinks i'm trying to add a option to a output. So I check on `cat --help` and google and found that if I use `cat --` I can override this to say *"hey we are going ignore operators"* 


---
## Notes


## Next Session
Continue to Level 10