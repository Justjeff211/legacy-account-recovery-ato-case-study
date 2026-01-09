# SOC Detection Rules: Account Recovery Abuse

## Rule 1: Excessive Account Recovery Attempts
Condition:
- Multiple password recovery attempts
- Same account
- Short time window
- Different IPs or devices

Severity: Medium to High  
MITRE: T1078 – Valid Accounts

## Rule 2: Password Reset Without MFA
Condition:
- Password reset event
- MFA not enforced
- New device or IP

Severity: High  
NIST: IA-2, IA-5

## Rule 3: Login After Password Reset from New Location
Condition:
- Login within 30 minutes of reset
- Geo-location anomaly

Severity: High  
MITRE: T1078 – Valid Accounts

## Rule 4: Cascading Password Resets
Condition:
- Multiple password resets
- Different platforms
- Same email account

Severity: Critical  
Impact: Full identity compromise

## Rule 5: Recovery Settings Changed Post-Reset
Condition:
- Recovery email or phone changed
- Shortly after password reset
- New device

Severity: Critical  
SOC Action: Immediate containment
