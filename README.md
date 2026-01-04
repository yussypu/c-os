## Key Concepts Demonstrated

**Virtual Memory**
- Two-level page tables (SV32)
- Page table entry format
- Virtual to physical translation
- TLB flushing with `sfence.vma`

**Process Management**
- Process control blocks
- State tracking (UNUSED, RUNNABLE)
- Stack allocation
- PID assignment

**Context Switching**
- Register preservation
- Stack pointer swapping
- Page table switching
- Kernel/user stack separation

**RISC-V Specifics**
- Supervisor mode operation
- CSR manipulation (satp, sscratch, stvec)
- Inline assembly for low-level ops
- Naked functions for entry points

## Limitations

- No preemption (processes must yield voluntarily)
- No syscall handling (traps panic)
- No user/kernel mode separation (everything runs in supervisor mode)
- No disk I/O or filesystem
- Fixed process limit
- Bump allocator (no free/realloc)
- No dynamic process creation after boot

This is educational code, not production-ready.

## Extending This

Natural next steps:
- Implement timer interrupts for preemption
- Add syscall handling (read, write, exit)
- Implement user mode with ecall interface
- Add ELF loading for arbitrary
