# python-file-io
An overengineered file IO database built in Python with automatic data clearing and input data validation

Features:
1. Self-healing file parser -- Auto-detect structural integrity issues in "data.txt" (e.g., incorrect field counts) and evicts the record from the database
2. Interactive data correction --  If a record contains invalid data, it will detect it and require users to update it
3. Data mapping -- Uses dictionaries to map indices to fields in the database
4. Persistence storage -- Allows users to save data back into "data.txt" for non-volatile storage

File Format Requirements (`/data.txt`)

The database expects data fields to be separated exactly by a triple-pipe (`|||`) delimiter in the following order:
Firstname|||Lastname|||DOB (DD-MM-YYYY)|||Home Phone|||Work Phone|||Mobile Phone|||Instagram Handle

Example row:
John|||Doe|||15-08-1998|||12345678|||87654321|||04123456|||@john_doe
