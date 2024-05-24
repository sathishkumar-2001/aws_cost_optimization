# aws_cost_optimization
IDENTIFYING THE AWS EC2 INSTANCE ATTACHED EBS VOLUME AND SNAPSHOT 
Identifying Stale EBS Snapshots and removing it

The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). 
For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. 
If it finds a stale snapshot,This code will now delete EBS snapshots that are older than 6 months and not attached to any volume or are attached to volumes that are not connected to any running instance it deletes it, 
effectively optimizing storage costs.
