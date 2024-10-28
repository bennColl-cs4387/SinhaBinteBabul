## Just the commands used to solve the mystery
    
    1   git clone https://github.com/nivbend/gitstery.git
    2  cd gitstery/
    3  ls
    4  cat instructions.txt
    5  git checkout gtpd-archive
    6  ls
    7  git log 
    8  git log -reverse
    9  git log --reverse
    10  git log --after="2019-07-01" --before="2019-08-01"
    11  git checkout detectives/kpumbinner
    12  ls
    13  cd evidence/
    14  ls
    15  cat access.log
    16  git blame access.log
    17  grep "BACKDOOR 332" access.log
    18  grep "BACKDOOR_332" access.log
    19  git blame access.log | grep "BACKDOOR_332" access.log
    20  git blame access.log | grep "BACKDOOR_332"
    21  ls
    22  cd ..
    23  ls
    24  grep "Brock Stuickard" residents.txt
    25  grep "Cosmo Siwkonk" residents.txt
    26  grep "Lyndon Huskupper" residents.txt
    27  git tag
    28  git checkout street/balcombe_close
    29  git log -n 10
    30  git checkout street/beaconside
    31  git log -n 10
    32  git checkout street/balcombe_close
    33  git log --skip 26
    34  git show bc6870d8093a33d9a69acc94a1cda16ee2d7195d
    35  git show c8411c73e49372dbdb644beef2ea841b403fc476
    36  git tag
    37  git checkout street/tamworth_drive
    38  git log --skip 76
    39  git log --skip 72
    40  git show f8a5b218b1eaee3b111ae5ef536f919e8d3afca2
    41  git show 22f733298423b814f1da31bee3e0063c72ed6e71
    42  echo "Cosmo Siwkonk" | git hash-object --stdin | grep -iq -f /dev/stdin <(git show solution) && echo 'You found the murderer!' || echo 'No cigar, chief... Try again.'
    43  cd ..
    44   history > history_for_print.txt
