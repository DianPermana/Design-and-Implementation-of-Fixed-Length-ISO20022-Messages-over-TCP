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
- Service Virtualization
  
# Step Procedure

- Open Apache JMeter 5.5
- Download Jar File From : https://github.com/DianPermana/Design-and-Implementation-of-Fixed-Length-ISO20022-Messages-over-TCP/blob/main/java-sampler-rsa-encryption-1.1-ISO-20022.jar
- store .Jar File to "...\apache-jmeter-5.5\apache-jmeter-5.5\lib\ext\java-sampler-rsa-encryption-1.1-ISO-20022.jar"
- Config : XML Format Message Request, Correlation Pattern, etc
- Run test Script

# Evidence Video

https://github.com/user-attachments/assets/3879df2d-a4f1-4477-b616-4cd1e2cc5529


# Thank You

- Dian Permana


