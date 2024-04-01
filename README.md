Check in terminal for certificates which can be used to sign the profile by using below command.
```ruby
security find-identity -v -p codesigning
```
Then use below command to sign the profile.
```ruby
/usr/bin/security cms -S -N "[Signing Certificate]" -i "[input]" -o "[output]"
security cms -S -N "iPhone Distribution: Thanh Bui Phan Cong (LKTAD7VQJ4)" -i enroll.mobileconfig -o sign.mobileconfig
```
EG: - /usr/bin/security cms -S -N "signing certificate(generally developer id)" -i 'path of unsigned profile' -o 'path of copy of unsigned profile'

