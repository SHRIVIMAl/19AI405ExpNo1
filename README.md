<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>
<h3>Name: T.K.SHRIVIMAL
<h3>Register Number:212224220101
<h3>Date : 15.10.2026


<h3>AIM:</h3>
<p>Treat unhealthy patients in each room. And check for the unhealthy patients in random room</p>
<h3>STEP 5:</h3>
<p>Measure the performance parameters: For each treatment performance incremented, for each movement performance decremented</p>

### PROGRAM:

```
import random
class HealthMonitoringAgent:
    def __init__(self, patient_data):
        self.patient_data = patient_data
    def monitor_health(self):
        while True:
            current_health_state = self.sensors.get_health_state()
            action = self.choose_action(current_health_state)
            self.actuators.perform_action(action)
            if self.choose_action(current_health_state)=="No specific action needed":
                break
    def choose_action(self, current_health_state):
        # Example: A simple rule-based system for decision-making
        if current_health_state['heart_rate'] > 120:
            return "Alert healthcare provider: High heart rate detected"
        elif current_health_state['blood_pressure'] > 140:
            return "Alert healthcare provider: High blood pressure detected"
        elif current_health_state['temperature'] > 38:
            return "Recommend rest and monitor temperature"
        else:
            return "No specific action needed"
class HealthSensors:
    def get_health_state(self):
        # Example: Simulate health data retrieval (replace with real data in a practical scenario)
        return {
            'heart_rate': random.randint(60, 150),
            'blood_pressure': random.randint(90, 160),
            'temperature': random.uniform(36.0, 38.5)
        }
class HealthActuators:
    def perform_action(self, action):
        # Example: Print or log the action (in a real scenario, this might involve more complex actions)
        print(action)
if __name__ == "__main__":
    patient_data = {'patient_id': 123, 'name': 'John Doe', 'age': 35}
    
    health_sensors = HealthSensors()
    health_actuators = HealthActuators()
    
    health_monitoring_agent = HealthMonitoringAgent(patient_data)
    health_monitoring_agent.sensors = health_sensors
    health_monitoring_agent.actuators = health_actuators
    
health_monitoring_agent.monitor_health()
```

### output:

<img width="1772" height="876" alt="image" src="https://github.com/user-attachments/assets/e9951853-2515-4663-9f66-d509c9a56c38" />


<img width="1086" height="645" alt="image" src="https://github.com/user-attachments/assets/35d1dbee-6100-4ea6-ab7a-3b5242bd3000" />


## Result:
Thus found the PEAS description for the given AI problem and develop an AI agent.
