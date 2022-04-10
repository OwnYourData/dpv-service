# SOyA DPV Service
version 0.1.0 (10.04.2022)

Build instructions:  
* `mvn clean install`
* `java -jar target/dpv-service-0.1.0-SNAPSHOT-jar-with-dependencies.jar`


## Usage Policy Matching Service  

### Instruction:  
The service is available at   
  - `http://localhost:2806/api/validate/usagepolicy`

Example usage: `curl -s -o /dev/null -w "%{http_code}" -H "Content-Type: application/json" -d "$(< src/test/resources/dpv/tester.json)" -X POST http://localhost:2806/api/validate/usagepolicy`  

### Input file format & response

The input file is of type `application/json` to wrap a turtle file using JSON key "usage-policy".  
There are four example turtle files in the `test/resources/dpv` directory for your references.

The output is `200` if the policy of controllers is not violating the policy of users, or `500` otherwise.


## Contact  
Contact `fajar.ekaputra@tuwien.ac.at` for further questions. 
