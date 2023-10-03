# IPv4-Fuscation

# Explaination
IPv4 addresses are 4 octets, this implementationt akes advantage of this to generate an IPv4 string with each byte as an octet. By converting each byte from hex to decimal for a single octet, we are able to turn hex shellcode into decimal format to obtain a (typically invalid) IPv4 address. For example, the first few bytes in Msfvenom payloads are typically the same. Using "FC 48 83 E4" as an example we can turn FC->252, 48->72, 83->131, E4->228, giving us 252.72.131.228 as our first octet. This requires the size of the payload to be obfuscated to be a multiple of four, padding payloads is possible, but not covered in this implementation. This is a method for evading static detection and will need to be deobfuscated in order for the payload to be executed.

# Drawbacks
I will not include the method to deobfuscate these payloads, but you can apply the same method for both IPv4 and IPv6 (also possible) obfuscation. Nor will I cover how to execute these payloads.

# Credit
Most code is from MalDev Academy, I will update this as I find more usage for it, however it was first seen being used by Hive Randsomeware Group.
