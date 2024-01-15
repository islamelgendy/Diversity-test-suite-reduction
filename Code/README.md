# Test-diversity

This tool is built for the experimental study to evaluate the effectiveness of 
diversity-based test suite reduction using string distance metrics.

Here we give simple instructions on how to use the tool to replicate the data.

1. If the compressed file is not in the standard format, you can run the "TestSuiteStandarizer" found in the "components" package. The working directory should be the parent folder of the compressed
 files. The tool can run through multiple folders each containing a compressed file and output them in the standard format for reduction.
2. To make the reduction, run the "DataLoader" found in the "components" package and input the required information. You must enter the complete path of the compressed test suite file. Also, for 
the similarity metric, you can enter the whole word of the metric, or only the first three letters. For example, you can enter "Hamming" or "Ham" to use the Hamming metric (case insensitive).
3. To run the analysis on the reduced test suites, you can run the bash script file "analysisScript.sh" and provide the directory of the test suites and the id of the project.
4. If the test suites are failing due to flaky tests or dependent tests, you can fix them and then run the analysis using the bash script file "fixAnalysisScript.sh" and provide the directory of the test suites and the id of the project.
5. Run the "TestParseResults" found in the "resultsanalysis" package to parse all information in the reduced test suites and put them in a CSV file.
6. Run the "SummarizeResults" found in the "resultsanalysis" package to summarize all of the CSV reports into a single CSV file to summarize the entire project.
