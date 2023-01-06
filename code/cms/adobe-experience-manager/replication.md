# AEM Replication

## Replication Process

- Publish content from the author to publish environment.
- Explicitly flush content from dispatcher cache
- Return user input from the publish environment to the author's environment

- author requests that certain content be published (activated).
- The request is passed to the appropriate default replication agent.
- The replication agent packages the content and places it in the replication queue.
- The content is lifted from the queue and transported to the publish environment using the configured protocol.
- A servlet in the publish environment receives the request and publishes the received content

Default servlet is: ```HTTP://LOCALHOST:4502/BIN/RECEIVE```

## Replication Agent

An replication agent has as it's responsibilities the following:

- Publish content from author into publish
- Flush content from dispatcher cache
- Return user input from the publish environment to the author environment

## Reverse Replication

Process of replicating content from publish environment into author environment. To accomplish this you'd need a reverse replication agent on the author instance, configured to get content from the publish environment outbox.

### Why You'd Need Reverse Replication

## Live Copy vs Language Copy

Live Copy -> Copy created from an existing site or blueprint. Rollout configurations for this Live Copy can be configured from the tools console.

Language Copy -> Site created using the language tool called Language Copy.

## Failing Replication

If the AEM replication fails, the following depends on the situation. If the replications are getting queued in the replication agent queues, you can check it by accessing the /etc/replications/agents.author.html and then click replication agents to analyse the situation.