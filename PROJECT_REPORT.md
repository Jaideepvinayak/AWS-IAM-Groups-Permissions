# AWS IAM Groups and Permissions

## 1. Objective
To create IAM groups, assign IAM users to the groups, configure permissions, and verify access using the AWS IAM Policy Simulator.

## 2. Tools and Services Used
- Amazon Web Services (AWS)
- AWS Identity and Access Management (IAM)
- IAM Users and Groups
- AWS Managed Policies
- IAM Policy Simulator

## 3. Implementation

### Step 1: Create IAM Groups
Created two IAM groups:
- Developers
- Auditors

### Step 2: Assign Permissions
Attached the following AWS managed policies:

| Group | Policy | Purpose |
|---|---|---|
| Developers | PowerUserAccess | Development access to AWS services |
| Auditors | ReadOnlyAccess | View AWS resources without modifying them |

### Step 3: Create IAM Users
Created two IAM users:
- developer1
- auditor1

Assigned each user to the corresponding IAM group.

### Step 4: Verify Group Membership
Verified that developer1 belongs to Developers and auditor1 belongs to Auditors.

### Step 5: Permission Simulation
Used the AWS IAM Policy Simulator to test S3 permissions.

Actions tested:
- ListAllMyBuckets
- CreateBucket

## 4. Expected Results

| User | Action | Expected Result |
|---|---|---|
| developer1 | ListAllMyBuckets | Allowed |
| auditor1 | ListAllMyBuckets | Allowed |
| developer1 | CreateBucket | Allowed |
| auditor1 | CreateBucket | Denied |

Actual simulation results should be checked against the recorded demonstration.

## 5. Conclusion
Successfully demonstrated IAM group creation, user assignment, permission management, and access verification using the AWS IAM Policy Simulator.

Group-based permission management helps simplify administration and improves access control in AWS.
