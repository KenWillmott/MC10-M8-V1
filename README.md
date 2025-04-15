# MC10-M8-V1
Basic TRS-80 MC-10 to M8 expansion interface
## Description
Allows one M8 peripheral expansion card to operate from the expansion port on the rear of the TRS-80 MC-10 microcomputer. The circuit decodes an I/O slot at 0xB400, so any M8 peripheral card will be addressed by the MC-10 at that location, plus any internal offset that the card uses. In order to prevent a hardware bus conflict when accessing those location, the SEL line on the MC-10 interface is activated to disable its internal devices mapped to the same locations.
Note: Gating with the CPU E signal is not performed by the interface card, it is always done on the M8 card. But, this is quite easy to do on the M8 card and some cards can do it without additional logic, since some I/O IC's perform E gating internally (such as 6522 VIA, Motorola MC6850, MC6821 etc.).
