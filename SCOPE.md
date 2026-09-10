# SCOPE

## Allowed targets

1. Repositories and systems owned by SmartVoltISA.
2. Local or isolated test deployments controlled by the project.
3. Explicitly authorized integrations and environments.
4. Public read-only interfaces where testing does not cross the stated boundary.
5. External bug-bounty targets only when the program explicitly authorizes the exact test and technique.

## Not allowed

- Unrelated third-party systems.
- Accounts or data without authorization.
- Destructive testing.
- Denial of service or intentional service degradation.
- Persistence, credential theft, data exfiltration, or irreversible changes.
- Treating public accessibility as permission to attack.

## Scope record

Every test case must record:

- target;
- repository and commit/version;
- environment;
- authorization basis;
- allowed techniques;
- prohibited techniques;
- test window when applicable;
- expected impact boundary.

## Principle

A vulnerability report is valid only inside the authorization boundary that allowed the test. Discovery outside scope is not a license to continue.
