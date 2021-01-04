cmake_minimum_required(VERSION 3.0.0)


include(ProcessorCount)
ProcessorCount(VAR)
message("Number of processors are: ${VAR}")
