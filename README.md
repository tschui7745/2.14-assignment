# 2.14-assignment
1.	Does SNS guarantee exactly once delivery to subscribers?

No, SNS does not guarantee exactly once delivery. It guarantees at least once delivery, which means messages will be delivered at least once, but duplicates can occur. This is because SNS retries message delivery in case of failures. If we need exactly once delivery or want to avoid duplicates, we will need to handle deduplication in the subscriber application.

2.	What is the purpose of the Dead-letter Queue (DLQ)? This a feature available to SQS/SNS/EventBridge.

The purpose of a Dead-letter Queue (DLQ) is to store messages that couldn’t be processed after several retries. It keeps failed messages safe, preventing loss and allowing us to investigate why they failed.

3.	How would you enable a notification to your email when messages are added to the DLQ?

To enable email notifications when messages are added to a Dead-letter Queue (DLQ), we can use Amazon CloudWatch Alarms combined with Amazon SNS.
