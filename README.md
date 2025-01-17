# Illumio Assessment

## Steps to Setup and Run
1. Download the contents of the repository into a folder
2. Set up Python on the local device
3. Run the file - Solution.ipynb

## To test
1. Change the input files:
   * lookup_table.csv - Enter look up table in .csv format
   * vpc_flow_log.txt - Provide log files in .txt format

## Program Metrics and details

### Data Structure:
1. Tags - Dictionary -> {tagname:counter}
2. Port, protocol, tags - Dictionary with Key as tuple and value as an array with tag as arr[0] and counter as arr[1] -> {(port,protocol):[tag,counter]}
3. Port, Protocol - Dictionary -> {port:protocol}
   
### Time Complexity 
Time Complexity for processing the flow logs is O(N) where N is the number of lines in the logs

### Space Complexity: 
Space Complexity is O(K) + O(L) where K is the number of lines in the lookup table, and L is the number of unique tags.

### Other Assumptions or Sources used
1. AWS VPC Flow Log record assumed to be of type: https://docs.aws.amazon.com/vpc/latest/userguide/flow-log-records.html
2. Port and Protocol mapping extracted as .csv from https://www.iana.org/assignments/protocol-numbers/protocol-numbers.xhtml
