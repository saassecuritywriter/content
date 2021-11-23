# OpsGenie

  
**OpsGenie** is a cloud based service that enables operations teams to manage alerts generated by monitoring tools to ensure the right people are notified, and the problems are addressed in a timely manner.  
  
Click **Add instance** to create and configure a new integration instance.  
1. Provide 'Server URL'. The default server URL should be sufficient for most cases.  
2. Provide 'API Key':    
    Retrieve your authentication token via the Teams API Integration section.  
3. Notice: if 'Query' is used - Status, Priority, Tags will be overided.  
  
In the following commands: `!opsgenie-create-alert`, `!opsgenie-add-responder-alert`, `!opsgenie-create-incident`, `!opsgenie-add-responder-incident`,   the *responders* argument **must** be List of triples.    
You need to insert it as List of triples in the next order: *responder_type, value_type, value*.    
The *responder_type* can be: team, user, escalation or schedule.    
The *value_type* can be: id or name.    
The *value* you can find from the output of the command `!opsgenie-get-teams`, `!opsgenie-get-schedules` or `!opsgenie-get-escalations`.    
For example: user,id,123,team,name,test_team.