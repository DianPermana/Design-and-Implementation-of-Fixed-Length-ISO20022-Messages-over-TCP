# Design-and-Implementation-of-Fixed-Length-ISO20022-Messages-over-TCP

The Goal of this project is how we send message ISO20022 XML Format via TCP using Apache JMeter & use Service virtualization to send back the results

# Tech Stack

- Apache JMeter 5.5
- java version "17.0.5" 2022-10-18 LTS
- Original source code : https://github.com/aboyfromipanema/java-sampler-rsa-encryption and why ? this is the answer https://www.blazemeter.com/blog/beanshell-vs-jsr223-vs-jmeter
  - Develope & Modify this Original source code based on : https://docs.developer.paynet.my/docs/credit-transfer/communication-protocol
    - Set-up all Parameter XML Format, date & time, UniqueId, etc as [pre-processor]
    - Send Message as [Execution]
    - Count Response Message with correlation as [Post-processor]
      - Example :
        - REQUEST_PATTERN : <ns2:EndToEndId>(.*?)</ns2:EndToEndId>
        - RESPONSE_PATTERN : <ns2:OrgnlEndToEndId>(.*?)</ns2:OrgnlEndToEndId>

# Step Procedure

- Open Apache JMeter 5.5
- Download Jar File From :
- store .Jar File to "...\apache-jmeter-5.5\apache-jmeter-5.5\lib\ext\java-sampler-rsa-encryption-1.1-ISO-20022.jar"
- Run test Script

# Evidence Video

https://github.com/user-attachments/assets/7775a98e-5c0a-4720-90ea-81161e904a83


# Thank You

- Dian Permana


