# Forensic Write Blocker

Oct 2, 2026 · @Jayesh Nitin Talele

## Project Overview

The Forensic Write Blocker is a software tool that lets investigators connect seized storage devices to a forensic workstation in read-only mode, so evidence can be examined without changing a single byte.

In digital forensics, evidence comes from hard disks, SSDs, pen drives, memory cards and phones. Simply plugging such a device into a computer can change it: the operating system may write logs, update timestamps or create hidden files. Any change can make the evidence unreliable in court.

The tool blocks every write operation to connected evidence devices, verifies the protection, calculates hash values to prove the data is unchanged, and keeps a complete log for each case.

**Who it is for**

- **Forensic examiners** — connect and examine seized devices safely in the lab.
- **Cyber cell investigators** — preview evidence quickly without altering it.
- **Lab supervisors** — review case logs and reports, and manage users.

**Key capabilities**

- Automatic detection of connected storage devices
- Read-only (write-protected) mounting of evidence devices
- Write-protection verification before examination
- Hash calculation (MD5, SHA-1, SHA-256) before and after examination
- Device details capture: model, serial number, capacity and partitions
- Case-wise activity log with timestamps
- Printable forensic report for court submission

## Challenges Before This Solution

Before this tool, examining a seized device risked changing the evidence itself, and there was little proof that the data stayed untouched.

1. **Accidental changes to evidence.** Connecting a device to a normal computer could alter files, timestamps or system areas without the examiner noticing.
2. **Evidence challenged in court.** If the defence could show the device was connected without protection, the evidence could be questioned or rejected.
3. **Costly hardware blockers.** Hardware write blockers are expensive and each one supports only certain interfaces, so labs had only a few to share.
4. **No proof of integrity.** Hash values were not always recorded before and after examination, so it was hard to prove the data had not changed.
5. **Manual record-keeping.** Device details and examination steps were written by hand, often with missing serial numbers or times.
6. **Slow field previews.** Investigators could not safely take a quick look at a device without waiting for the lab.
7. **Inconsistent procedure.** Each examiner followed their own steps, so results and documentation varied between cases.

## The Solution

The tool turns any forensic workstation into a safe examination station: devices are locked to read-only, the lock is verified, and hash values prove the evidence never changed.

| Challenge | How the tool solves it |
| --- | --- |
| Accidental changes to evidence | Every connected storage device is mounted read-only; all write requests are blocked |
| Evidence challenged in court | Logged proof that protection was active for the whole session |
| Costly hardware blockers | Software protection on any workstation, for USB, SATA and memory-card devices |
| No proof of integrity | Hash values calculated at the start and end and compared automatically |
| Manual record-keeping | Device model, serial number, capacity and partitions captured automatically |
| Slow field previews | Safe read-only preview on a laptop at the scene or in the cyber cell |
| Inconsistent procedure | A fixed, step-by-step workflow with a standard report for every case |

**Core modules**

- **Case Management** — create a case with case number, examiner and evidence details.
- **Device Detection** — detect connected devices and read their technical details.
- **Write Protection** — switch protection on for selected devices and keep it on.
- **Protection Verification** — run a safe test that confirms writes are blocked.
- **Hash Verification** — calculate and compare MD5, SHA-1 and SHA-256 values.
- **Activity Log** — time-stamped record of every action in the session.
- **Reports** — generate a signed forensic report in PDF.

## Flow Pages

The tool runs in 10 screens that take a device from detection to a signed report, and examination is allowed only after protection is verified.

&#91;embedded content: evidence handling flow · 10 screens\]

If the verification test fails, the examiner must re-enable protection and verify again before going further.

1. **Login** — Secure sign-in for authorised examiners; every action is recorded against the user.
2. **Dashboard** — Open cases, devices currently connected, their protection status and recent activity.
3. **Create Case** — Enter case number, FIR or reference number, examiner name and evidence ID.
4. **Device Detection** — The tool lists connected storage devices with model, serial number, capacity, interface and partitions.
5. **Enable Write Protection** — The examiner selects the evidence device and switches it to read-only mode.
6. **Verify Protection** — The tool runs a safe test to confirm writes are blocked and records the result.
7. **Initial Hash** — MD5, SHA-1 and SHA-256 values of the device are calculated and saved before examination.
8. **Examine or Image** — The examiner browses and copies files, or creates a full forensic image, with the original untouched.
9. **Final Hash Check** — Hash values are calculated again and compared with the initial values to prove nothing changed.
10. **Report** — A forensic report with case details, device details, verification result, hash values and the activity log, exported as a signed PDF.

## FAQs (Frequently Asked Questions)

**1. What is a write blocker?** A write blocker lets a computer read data from a storage device while preventing any change to it. It protects digital evidence from being altered during examination.

**2. Why is it important in forensics?** Courts need proof that digital evidence is exactly as it was when seized. A write blocker, along with hash verification, provides that proof.

**3. Which devices does it support?** Internal and external hard disks, SSDs, pen drives and memory cards connected through USB, SATA or card readers.

**4. How do I know the protection is working?** The tool runs a verification test after protection is switched on. It attempts a safe test write, confirms it was blocked, and records the result in the log.

**5. What is a hash value?** A hash value is a unique digital fingerprint of the data. If even one bit changes, the hash changes. Matching hashes before and after examination prove the evidence is unchanged.

**6. Can I examine or copy files while protection is on?** Yes. You can browse, view and copy data from the device, or create a forensic image, with no changes made to the original.

**7. What happens if protection is switched off by mistake?** Protection cannot be switched off for an evidence device during an active case session without supervisor approval, and any such action is logged.

**8. Does it replace a hardware write blocker?** It is a cost-effective alternative for many cases and for field previews. Labs can still use hardware blockers where their procedures require it.

**9. What does the forensic report contain?** Case details, examiner name, device details, protection status, verification result, hash values, the activity log and timestamps.

**10. Who can use the tool?** Only authorised forensic examiners and investigators with login credentials. Every action is recorded against the user.
