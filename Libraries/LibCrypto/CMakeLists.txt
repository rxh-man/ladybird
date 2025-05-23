add_cxx_compile_options(-Wvla)

set(SOURCES
    AEAD/ChaCha20Poly1305.cpp
    ASN1/ASN1.cpp
    ASN1/DER.cpp
    ASN1/PEM.cpp
    Authentication/GHash.cpp
    Authentication/Poly1305.cpp
    BigFraction/BigFraction.cpp
    BigInt/Algorithms/BitwiseOperations.cpp
    BigInt/Algorithms/Division.cpp
    BigInt/Algorithms/GCD.cpp
    BigInt/Algorithms/ModularInverse.cpp
    BigInt/Algorithms/ModularPower.cpp
    BigInt/Algorithms/Multiplication.cpp
    BigInt/Algorithms/SimpleOperations.cpp
    BigInt/SignedBigInteger.cpp
    BigInt/UnsignedBigInteger.cpp
    Certificate/Certificate.cpp
    Checksum/Adler32.cpp
    Checksum/cksum.cpp
    Checksum/CRC32.cpp
    Cipher/AES.cpp
    Cipher/Cipher.cpp
    Cipher/ChaCha20.cpp
    Curves/Curve25519.cpp
    Curves/Ed25519.cpp
    Curves/X25519.cpp
    Curves/X448.cpp
    Hash/BLAKE2b.cpp
    Hash/MD5.cpp
    Hash/SHA1.cpp
    Hash/SHA2.cpp
    NumberTheory/ModularFunctions.cpp
    PK/RSA.cpp
    PK/EC.cpp
)

serenity_lib(LibCrypto crypto)
target_link_libraries(LibCrypto PRIVATE LibCore)
