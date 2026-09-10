The bus, or communication system, connecting the CPU, memory controller, and memory devices has two main pathways: data and address.

- **Data Pathway:** Determines the amount of information transferred per clock cycle. In a single channel memory controller, this bus is typically 64 bits wide.
    
- **Address Pathway:** Determines the number of memory locations the CPU can track, thus limiting the maximum physical and virtual memory.
    
    - A 32-bit CPU with a 32-bit address bus can access up to 4 GB of memory.
        
    - A 64-bit CPU could theoretically use a 64-bit address space (16 exabytes), but most use a 48-bit address bus, allowing up to 256 terabytes of memory.