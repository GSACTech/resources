# Report format explained for participants of [Global Software Analysis Competition](https://gsac.tech/)

* This is a report file with a valid structure but completed with invalid values to explain what is
  expected in each field

* For any discussion follow the [link](https://github.com/GSACTech/contest/discussions)
* Here is a list of some required fields with their explanation
    * `tool` - this contains the needed information about the analyzer
        * `rules` - this array contains all rules which have this analyzer and additional
          information about those rules
        * `id` - for each rule there's an id which is a string, like its name, those ids will be
          used in reports
    * `results` - this array contains all results which are reported by analyzer
        * `ruleId` - each report has rule id, which must exist in `rules`
        * `ruleIndex` - this is the corresponding index in `rules` array(started from 0)
        * `locations` - in our context this is expected to be an array of only one element which is
          the last instruction where the error occurred(additional information is written in
          report.sarif
          file)
        * `codeFlows->threadFlows->locations` - similar to previous one but here we have two
          locations in this array(in report.sarif everything is explained)
