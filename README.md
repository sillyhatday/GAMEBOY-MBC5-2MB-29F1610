# GAMEBOY-FLASHCART-MBC5-29F1610-2MB

A working PCB layout for making your own MBC5 2MB based Gameboy cartridge. I've sat on this project for years. I could not get the flash to program for a long time, so I gave up on it as it has limited use. A few years ago I got the chip to program in FlashGBX under the BungDoctor profile. In the newer versions the cartridge is correctly detected as such and should not need manually setting.

>[!NOTE]
>If the cart is not detected as writable, manually select the BungDoctor cartridge in FlashGBX

## ⚪ Game Compatibility

Nearly all Gameboy colour games used this memory mapper. It can address up to 8MB of game storage and up to 128KB of game save storage. This one only using 2MB of ROM and 32KB of RAM. 95% of GBC games using this mapper are within this range. Most 8KB save files should work fine on the 32KB chip also. 

Earlier games from the DMG should work, Nintendo kept each revision of mapper compatible with the previous (for the most part). So long as programmers followed Nintendos suggestions when developing. Mole Mania wasn't designed for an MBC5 and works perfectly, yet Zelda - Links Awakening doesn't, it crashes when saving.


>[!WARNING]
>This cart will not work properly for real time clock games. This means games like Pokemon G/S/C.

## 📷 Photos

<img width="800" height="782" alt="CartFront" src="https://github.com/user-attachments/assets/c10022de-8679-40fc-9f5c-40e039d7e32c" />

<img width="800" height="742" alt="Gameboy MBC5 Cart + FRAM" src="https://github.com/user-attachments/assets/37e35b22-549e-4a6e-a835-414b7ef78861" />

## 🟣 Bill of materials:

>[!IMPORTANT]
>When ordering PCBs, be sure to order in 0.8mm thickness with gold plating!

| Part | Quantity |
|--------------|----|
| 29F1610 Flash | x1 |
| FM1808 or FM18W08* | x1 |
| MBC5 | x1 |
| SN74LVC1G332DBVR | x1 |
| 10K 0603 resistor | x2 |
| 0.1uF 0603 capacitor | x4 |

**FM18L08 will work but is not suggested*

### 💻 EEPROM 29F1610 <br>
I found these were really cheap as an alternative to the usual 5v chips used. They are not that available and not often that cheap, around €2 per chip. These are a 16-bit address and 8/16-bit data bus EEPROM. They can be configured to us word/byte mode. The write enable pin is brought to the audio pin on the Gameboy cartridge header. This is compatible with the GBxCart RW. The pin is held to 5v to keep it disabled during usage through a pullup resistor.

### 🐏 FRAM FM1808 <br>
These are expensive. Current prices are €11.90 from Mouser. They are available for much less on Aliexpress, for the same price you can get 5 - 10. These are known to be ***extremely*** unreliable. You are likely buying factory rejects that don't fully work or meet the speed rating. In a batch of 5 from Aliexpress I got, none of them worked. Another 10 I got, I went through 4 before finding a working one. In the end I went through 8 chips before getting one that works. The cost of 9 dodgy chips was more than one from Mouser.

### ❗OR Gate SN74LVC1G332DBVR
I consider this optional but reccomended. In my testing, I have not found that games under 2MB in size require extra glue logic. I'd still use it to be confident that your game saves will be safe.

### ❔ Memory Controller MBC5 <br>
You used to be able to go on eBay and find trash games for €3 easily, some deals I've had as low as €1. I could go on eBay and grab one or two of them per week. They seem to have gone up and the best deals are about €5 now. You'll need a hot air station to remove the chip from the board.

## Links

🏷️ NextStopPlease Labels: https://nextstopplease.square.site/ <br>
📷 NextStopPlease Insta: https://www.instagram.com/nxt.stop.please/ <br>
🛍️ Inside Gadgets Shop: https://shop.insidegadgets.com <br>
📎 Inside Gadgets GitHub: https://github.com/insidegadgets <br>
📷 Inside Gadgets Insta: https://www.instagram.com/inside.gadgets <br>
🖇️ Bytendo Mods GitHub: https://github.com/bytendomods <br>
🐭 Bucket Mouse: https://github.com/Bucket-Mouse <br>
🛒 Natalie Shop: https://nataliethenerd.com/ <br>
🤓 Natalie GitHub: https://github.com/natalie-lang/natalie <br>

## ⚖️ License

This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License. You are able to copy and redistribute the material in any medium or format, as well as remix, transform, or build upon the material for any purpose (even commercial) - but you must give appropriate credit, provide a link to the license, and indicate if any changes were made.

