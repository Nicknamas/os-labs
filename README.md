# os-labs

# Лабораторная работа №1

<img width="830" height="461" alt="image" src="https://github.com/user-attachments/assets/e6c8e938-68af-4510-be85-19e9463ccc63" />

<img width="812" height="233" alt="image" src="https://github.com/user-attachments/assets/82ba7025-0f7a-43be-8e45-dce3b5bf2cf9" />

## main_O0.s
```c
	.file	"main.c"
	.text
.Ltext0:
	.file 0 "/home/woadex/Work/pets/os" "main.c"
	.globl	compute_factorial
	.type	compute_factorial, @function
compute_factorial:
.LFB0:
	.file 1 "main.c"
	.loc 1 3 30
	.cfi_startproc
	pushq	%rbp
	.cfi_def_cfa_offset 16
	.cfi_offset 6, -16
	movq	%rsp, %rbp
	.cfi_def_cfa_register 6
	movl	%edi, -20(%rbp)
	.loc 1 4 9
	movl	$1, -4(%rbp)
.LBB2:
	.loc 1 5 14
	movl	$1, -8(%rbp)
	.loc 1 5 5
	jmp	.L2
.L3:
	.loc 1 6 16
	movl	-4(%rbp), %eax
	imull	-8(%rbp), %eax
	movl	%eax, -4(%rbp)
	.loc 1 5 30 discriminator 3
	addl	$1, -8(%rbp)
.L2:
	.loc 1 5 23 discriminator 1
	movl	-8(%rbp), %eax
	cmpl	-20(%rbp), %eax
	jle	.L3
.LBE2:
	.loc 1 8 12
	movl	-4(%rbp), %eax
	.loc 1 9 1
	popq	%rbp
	.cfi_def_cfa 7, 8
	ret
	.cfi_endproc
.LFE0:
	.size	compute_factorial, .-compute_factorial
	.section	.rodata
.LC0:
	.string	"Factorial of %d is %d\n"
	.text
	.globl	main
	.type	main, @function
main:
.LFB1:
	.loc 1 11 12
	.cfi_startproc
	pushq	%rbp
	.cfi_def_cfa_offset 16
	.cfi_offset 6, -16
	movq	%rsp, %rbp
	.cfi_def_cfa_register 6
	subq	$16, %rsp
	.loc 1 12 9
	movl	$5, -4(%rbp)
	.loc 1 13 16
	movl	-4(%rbp), %eax
	movl	%eax, %edi
	call	compute_factorial
	movl	%eax, -8(%rbp)
	.loc 1 14 5
	movl	-8(%rbp), %edx
	movl	-4(%rbp), %eax
	movl	%eax, %esi
	movl	$.LC0, %edi
	movl	$0, %eax
	call	printf
	.loc 1 15 12
	movl	$0, %eax
	.loc 1 16 1
	leave
	.cfi_def_cfa 7, 8
	ret
	.cfi_endproc
.LFE1:
	.size	main, .-main
.Letext0:
	.file 2 "/usr/include/stdio.h"
	.section	.debug_info,"",@progbits
.Ldebug_info0:
	.long	0x127
	.value	0x5
	.byte	0x1
	.byte	0x8
	.long	.Ldebug_abbrev0
	.uleb128 0x3
	.long	.LASF13
	.byte	0x1d
	.byte	0x3
	.long	0x31647
	.long	.LASF0
	.long	.LASF1
	.quad	.Ltext0
	.quad	.Letext0-.Ltext0
	.long	.Ldebug_line0
	.uleb128 0x1
	.byte	0x8
	.byte	0x7
	.long	.LASF2
	.uleb128 0x1
	.byte	0x4
	.byte	0x7
	.long	.LASF3
	.uleb128 0x1
	.byte	0x1
	.byte	0x8
	.long	.LASF4
	.uleb128 0x1
	.byte	0x2
	.byte	0x7
	.long	.LASF5
	.uleb128 0x1
	.byte	0x1
	.byte	0x6
	.long	.LASF6
	.uleb128 0x1
	.byte	0x2
	.byte	0x5
	.long	.LASF7
	.uleb128 0x4
	.byte	0x4
	.byte	0x5
	.string	"int"
	.uleb128 0x1
	.byte	0x8
	.byte	0x5
	.long	.LASF8
	.uleb128 0x1
	.byte	0x1
	.byte	0x6
	.long	.LASF9
	.uleb128 0x5
	.long	0x6b
	.uleb128 0x6
	.byte	0x8
	.long	0x72
	.uleb128 0x7
	.long	.LASF14
	.byte	0x2
	.value	0x16e
	.byte	0xc
	.long	0x5d
	.long	0x95
	.uleb128 0x8
	.long	0x77
	.uleb128 0x9
	.byte	0
	.uleb128 0xa
	.long	.LASF15
	.byte	0x1
	.byte	0xb
	.byte	0x5
	.long	0x5d
	.quad	.LFB1
	.quad	.LFE1-.LFB1
	.uleb128 0x1
	.byte	0x9c
	.long	0xd2
	.uleb128 0x2
	.long	.LASF10
	.byte	0xc
	.long	0x5d
	.uleb128 0x2
	.byte	0x91
	.sleb128 -20
	.uleb128 0x2
	.long	.LASF11
	.byte	0xd
	.long	0x5d
	.uleb128 0x2
	.byte	0x91
	.sleb128 -24
	.byte	0
	.uleb128 0xb
	.long	.LASF16
	.byte	0x1
	.byte	0x3
	.byte	0x5
	.long	0x5d
	.quad	.LFB0
	.quad	.LFE0-.LFB0
	.uleb128 0x1
	.byte	0x9c
	.uleb128 0xc
	.string	"n"
	.byte	0x1
	.byte	0x3
	.byte	0x1b
	.long	0x5d
	.uleb128 0x2
	.byte	0x91
	.sleb128 -36
	.uleb128 0x2
	.long	.LASF12
	.byte	0x4
	.long	0x5d
	.uleb128 0x2
	.byte	0x91
	.sleb128 -20
	.uleb128 0xd
	.quad	.LBB2
	.quad	.LBE2-.LBB2
	.uleb128 0xe
	.string	"i"
	.byte	0x1
	.byte	0x5
	.byte	0xe
	.long	0x5d
	.uleb128 0x2
	.byte	0x91
	.sleb128 -24
	.byte	0
	.byte	0
	.byte	0
	.section	.debug_abbrev,"",@progbits
.Ldebug_abbrev0:
	.uleb128 0x1
	.uleb128 0x24
	.byte	0
	.uleb128 0xb
	.uleb128 0xb
	.uleb128 0x3e
	.uleb128 0xb
	.uleb128 0x3
	.uleb128 0xe
	.byte	0
	.byte	0
	.uleb128 0x2
	.uleb128 0x34
	.byte	0
	.uleb128 0x3
	.uleb128 0xe
	.uleb128 0x3a
	.uleb128 0x21
	.sleb128 1
	.uleb128 0x3b
	.uleb128 0xb
	.uleb128 0x39
	.uleb128 0x21
	.sleb128 9
	.uleb128 0x49
	.uleb128 0x13
	.uleb128 0x2
	.uleb128 0x18
	.byte	0
	.byte	0
	.uleb128 0x3
	.uleb128 0x11
	.byte	0x1
	.uleb128 0x25
	.uleb128 0xe
	.uleb128 0x13
	.uleb128 0xb
	.uleb128 0x90
	.uleb128 0xb
	.uleb128 0x91
	.uleb128 0x6
	.uleb128 0x3
	.uleb128 0x1f
	.uleb128 0x1b
	.uleb128 0x1f
	.uleb128 0x11
	.uleb128 0x1
	.uleb128 0x12
	.uleb128 0x7
	.uleb128 0x10
	.uleb128 0x17
	.byte	0
	.byte	0
	.uleb128 0x4
	.uleb128 0x24
	.byte	0
	.uleb128 0xb
	.uleb128 0xb
	.uleb128 0x3e
	.uleb128 0xb
	.uleb128 0x3
	.uleb128 0x8
	.byte	0
	.byte	0
	.uleb128 0x5
	.uleb128 0x26
	.byte	0
	.uleb128 0x49
	.uleb128 0x13
	.byte	0
	.byte	0
	.uleb128 0x6
	.uleb128 0xf
	.byte	0
	.uleb128 0xb
	.uleb128 0xb
	.uleb128 0x49
	.uleb128 0x13
	.byte	0
	.byte	0
	.uleb128 0x7
	.uleb128 0x2e
	.byte	0x1
	.uleb128 0x3f
	.uleb128 0x19
	.uleb128 0x3
	.uleb128 0xe
	.uleb128 0x3a
	.uleb128 0xb
	.uleb128 0x3b
	.uleb128 0x5
	.uleb128 0x39
	.uleb128 0xb
	.uleb128 0x27
	.uleb128 0x19
	.uleb128 0x49
	.uleb128 0x13
	.uleb128 0x3c
	.uleb128 0x19
	.uleb128 0x1
	.uleb128 0x13
	.byte	0
	.byte	0
	.uleb128 0x8
	.uleb128 0x5
	.byte	0
	.uleb128 0x49
	.uleb128 0x13
	.byte	0
	.byte	0
	.uleb128 0x9
	.uleb128 0x18
	.byte	0
	.byte	0
	.byte	0
	.uleb128 0xa
	.uleb128 0x2e
	.byte	0x1
	.uleb128 0x3f
	.uleb128 0x19
	.uleb128 0x3
	.uleb128 0xe
	.uleb128 0x3a
	.uleb128 0xb
	.uleb128 0x3b
	.uleb128 0xb
	.uleb128 0x39
	.uleb128 0xb
	.uleb128 0x27
	.uleb128 0x19
	.uleb128 0x49
	.uleb128 0x13
	.uleb128 0x11
	.uleb128 0x1
	.uleb128 0x12
	.uleb128 0x7
	.uleb128 0x40
	.uleb128 0x18
	.uleb128 0x7c
	.uleb128 0x19
	.uleb128 0x1
	.uleb128 0x13
	.byte	0
	.byte	0
	.uleb128 0xb
	.uleb128 0x2e
	.byte	0x1
	.uleb128 0x3f
	.uleb128 0x19
	.uleb128 0x3
	.uleb128 0xe
	.uleb128 0x3a
	.uleb128 0xb
	.uleb128 0x3b
	.uleb128 0xb
	.uleb128 0x39
	.uleb128 0xb
	.uleb128 0x27
	.uleb128 0x19
	.uleb128 0x49
	.uleb128 0x13
	.uleb128 0x11
	.uleb128 0x1
	.uleb128 0x12
	.uleb128 0x7
	.uleb128 0x40
	.uleb128 0x18
	.uleb128 0x7a
	.uleb128 0x19
	.byte	0
	.byte	0
	.uleb128 0xc
	.uleb128 0x5
	.byte	0
	.uleb128 0x3
	.uleb128 0x8
	.uleb128 0x3a
	.uleb128 0xb
	.uleb128 0x3b
	.uleb128 0xb
	.uleb128 0x39
	.uleb128 0xb
	.uleb128 0x49
	.uleb128 0x13
	.uleb128 0x2
	.uleb128 0x18
	.byte	0
	.byte	0
	.uleb128 0xd
	.uleb128 0xb
	.byte	0x1
	.uleb128 0x11
	.uleb128 0x1
	.uleb128 0x12
	.uleb128 0x7
	.byte	0
	.byte	0
	.uleb128 0xe
	.uleb128 0x34
	.byte	0
	.uleb128 0x3
	.uleb128 0x8
	.uleb128 0x3a
	.uleb128 0xb
	.uleb128 0x3b
	.uleb128 0xb
	.uleb128 0x39
	.uleb128 0xb
	.uleb128 0x49
	.uleb128 0x13
	.uleb128 0x2
	.uleb128 0x18
	.byte	0
	.byte	0
	.byte	0
	.section	.debug_aranges,"",@progbits
	.long	0x2c
	.value	0x2
	.long	.Ldebug_info0
	.byte	0x8
	.byte	0
	.value	0
	.value	0
	.quad	.Ltext0
	.quad	.Letext0-.Ltext0
	.quad	0
	.quad	0
	.section	.debug_line,"",@progbits
.Ldebug_line0:
	.section	.debug_str,"MS",@progbits,1
.LASF3:
	.string	"unsigned int"
.LASF16:
	.string	"compute_factorial"
.LASF2:
	.string	"long unsigned int"
.LASF9:
	.string	"char"
.LASF11:
	.string	"fact"
.LASF4:
	.string	"unsigned char"
.LASF15:
	.string	"main"
.LASF12:
	.string	"result"
.LASF8:
	.string	"long int"
.LASF5:
	.string	"short unsigned int"
.LASF14:
	.string	"printf"
.LASF10:
	.string	"micro_var"
.LASF7:
	.string	"short int"
.LASF6:
	.string	"signed char"
.LASF13:
	.string	"GNU C23 15.2.1 20260123 (Red Hat 15.2.1-7) -mtune=generic -march=x86-64 -g2 -O0"
	.section	.debug_line_str,"MS",@progbits,1
.LASF1:
	.string	"/home/woadex/Work/pets/os"
.LASF0:
	.string	"main.c"
	.ident	"GCC: (GNU) 15.2.1 20260123 (Red Hat 15.2.1-7)"
	.section	.note.GNU-stack,"",@progbits

```

## main_O2.s
```c
	.file	"main.c"                     # Имя исходного файла C
	.text                              # Секция кода (инструкции процессора)
	.p2align 4                         # Выравнивание следующего кода на 16 байт для быстрой выборки процессором
	.globl	compute_factorial          # Делает метку глобальной (видимой для линкера)
	.type	compute_factorial, @function # Объявляет метку как функцию
compute_factorial:
.LFB11:
	.cfi_startproc                    # Начало отладочной структуры вызова (Call Frame Information)
	testl	%edi, %edi                # Проверяет аргумент 'n' (в регистре edi). По сути: n == 0 или n < 0?
	jle	.L4                       # Если n <= 0, прыгаем на .L4 (возвращаем 1)
	leal	1(%rdi), %esi             # Вычисляет n + 1 и сохраняет в esi. Это верхняя граница для цикла
	andl	$1, %edi                  # Проверяет четность n (остаток от деления на 2). edi = n & 1
	movl	$1, %eax                  # Инициализирует счетчик цикла: eax = 1
	movl	$1, %edx                  # Инициализирует накопитель результата: edx = 1 (result = 1)
	je	.L3                       # Если n четное (результат andl равен 0), прыгаем сразу в цикл .L3
	movl	$2, %eax                  # Если n нечетное: сдвигаем стартовый счетчик eax = 2
	cmpl	%esi, %eax                # Сравниваем счетчик (2) с верхней границей (n + 1)
	je	.L1                       # Если они равны (было n=1), пропускаем цикл и прыгаем на выход .L1
	.p2align 4                        # Директивы выравнивания памяти
	.p2align 4                        # Нужны для того, чтобы начало цикла .L3
	.p2align 3                        # попало на оптимальный адрес в кэше процессора
.L3:                                      # ГЛАВНЫЙ ЦИКЛ (развернут: считает по 2 шага за итерацию)
	imull	%eax, %edx                # Умножаем: edx = edx * eax (текущий шаг)
	leal	1(%rax), %ecx             # Вычисляем следующий шаг: ecx = eax + 1
	addl	$2, %eax                  # Увеличиваем счетчик сразу на два: eax = eax + 2
	imull	%ecx, %edx                # Умножаем на следующий шаг: edx = edx * ecx
	cmpl	%esi, %eax                # Проверяем условие: счетчик eax дошел до границы esi (n + 1)?
	jne	.L3                       # Если не равен (!=), повторяем цикл .L3
.L1:                                      # ВЫХОД ИЗ ЦИКЛА (при успешном расчете)
	movl	%edx, %eax                # Переносим итоговый результат из edx в регистр возврата eax
	ret                               # Возврат из функции
	.p2align 4,,10                    # Выравнивание памяти перед следующей меткой
	.p2align 3
.L4:                                      # ОБРАБОТКА СЛУЧАЯ n <= 0 или n=1 (базовый случай)
	movl	$1, %edx                  # Помещаем 1 в edx (результат = 1)
	movl	%edx, %eax                # Переносим 1 в регистр возврата eax
	ret                               # Возврат из функции
	.cfi_endproc                      # Конец отладочной структуры вызова
.LFE11:
	.size	compute_factorial, .-compute_factorial # Вычисление размера функции в байтах
	.section	.rodata.str1.1,"aMS",@progbits,1 # Секция данных "только для чтения" (Read-Only Data)
.LC0:
	.string	"Factorial of %d is %d\n"  # Строка формата для printf
	.section	.text.startup,"ax",@progbits # Секция кода, выполняемая при запуске
	.p2align 4                        # Выравнивание кода по границе 16 байт
	.globl	main                      # Делает метку main глобальной
	.type	main, @function           # Объявляет метку как функцию
main:
.LFB12:
	.cfi_startproc                    # Начало отладочной структуры для main
	subq	$8, %rsp                  # Выравниваем указатель стека (требование ABI для вызова функций)
	.cfi_def_cfa_offset 16
	movl	$120, %edx                # ОПТИМИЗАЦИЯ: Сразу загружаем 120 (результат 5!) в 3-й аргумент (edx)
	movl	$5, %esi                  # Загружаем число 5 во 2-й аргумент (esi) для printf
	xorl	%eax, %eax                # Обнуляем eax (указывает printf, что аргументов-флоатов в SSE нет)
	movl	$.LC0, %edi               # Загружаем адрес строки формата в 1-й аргумент (edi)
	call	printf                    # Вызываем системную функцию printf
	xorl	%eax, %eax                # Обнуляем eax перед выходом (return 0;)
	addq	$8, %rsp                  # Восстанавливаем указатель стека в исходное состояние
	.cfi_def_cfa_offset 8
	ret                               # Завершаем программу (выход из main)
	.cfi_endproc                      # Конец отладочной структуры
.LFE12:
	.size	main, .-main              # Вычисление размера функции main
	.ident	"GCC: (GNU) 15.2.1 20260123 (Red Hat 15.2.1-7)" # Маркер версии компилятора
	.section	.note.GNU-stack,"",@progbits # Пометка для ОС: стек не должен быть исполняемым
```

## Работа с Makefile
<img width="1381" height="290" alt="image" src="https://github.com/user-attachments/assets/04cc6ecb-83f1-4e60-ba38-fa93a6db43e0" />
<img width="1381" height="290" alt="image" src="https://github.com/user-attachments/assets/fb30e600-397d-4233-ad7f-ad4bfdd55aa3" />
<img width="1381" height="290" alt="image" src="https://github.com/user-attachments/assets/87a27f8c-dcad-4520-821c-80d01f45b3f1" />
<img width="1442" height="268" alt="image" src="https://github.com/user-attachments/assets/7c561847-9a9c-4900-a4e4-9aa7d146b50b" />
<img width="681" height="430" alt="image" src="https://github.com/user-attachments/assets/41908608-d2cf-4265-9c46-7dd4a989ade2" />

# Работа с параллельностью
<img width="1248" height="350" alt="image" src="https://github.com/user-attachments/assets/63e4e43b-6b30-40a7-aac7-b1278720da88" />

```c
#include <stdio.h>
#include <stdlib.h>
#include <unistd.h>
#include <fcntl.h>
#include <sys/mman.h>
#include <sys/wait.h>
#include <semaphore.h>
#include "factorial.h"

int main() {
    sem_t *sem = mmap(NULL, sizeof(sem_t), PROT_READ | PROT_WRITE, 
                      MAP_SHARED | MAP_ANONYMOUS, -1, 0);
    
    if (sem == MAP_FAILED) {
        perror("mmap failed");
        return 1;
    }

    sem_init(sem, 1, 1);

    pid_t pid = fork();

    if (pid < 0) {
        perror("fork failed");
        return 1;
    }

    if (pid == 0) {
        for (int i = 1; i <= 3; i++) {
            sem_wait(sem);
            
            FILE *f = fopen("output.txt", "a");
            if (f) {
                fprintf(f, "[Потомок PID %d] Вычисляю факт %d: %d\n", 
                        getpid(), i, compute_factorial(i));
                fclose(f);
            }
            
            sem_post(sem);
            sleep(1); 
        }
        exit(0);
    } else {
        for (int i = 4; i <= 6; i++) {
            sem_wait(sem);
            
            FILE *f = fopen("output.txt", "a");
            if (f) {
                fprintf(f, "[Родитель PID %d] Вычисляю факт %d: %d\n", 
                        getpid(), i, compute_factorial(i));
                fclose(f);
            }
            
            sem_post(sem);
            sleep(1);
        }

        wait(NULL);
    }

    sem_destroy(sem);
    munmap(sem, sizeof(sem_t));
    
    printf("Работа завершена. Проверьте файл output.txt\n");
    return 0;
}
```

## Доработанный Makefile

```Makefile
CC = gcc
CFLAGS = -Wall -O2
ASM_FLAGS_O0 = -S -O0 -g2
ASM_FLAGS_O2 = -S -O2

all: asm_files app parallel_app

asm_files: main_O0.s main_O2.s

main_O0.s: main.c
	$(CC) $(ASM_FLAGS_O0) -o main_O0.s main.c

main_O2.s: main.c
	$(CC) $(ASM_FLAGS_O2) -o main_O2.s main.c

app: main_modular.o factorial.o
	$(CC) $(CFLAGS) -o app main_modular.o factorial.o

main_modular.o: main_modular.c factorial.h
	$(CC) $(CFLAGS) -c main_modular.c

factorial.o: factorial.c factorial.h
	$(CC) $(CFLAGS) -c factorial.c

parallel_app: parallel_sync.o factorial.o
	$(CC) $(CFLAGS) -o parallel_app parallel_sync.o factorial.o -pthread

parallel_sync.o: parallel_sync.c factorial.h
	$(CC) $(CFLAGS) -c parallel_sync.c

clean:
	rm -f *.o app parallel_app main_O0.s main_O2.s output.txt
```

# Лабараторная работа №2


https://rutube.ru/video/1cab14af110d8989e8b836b22e2974ad/


# Лабараторная работа №3a
<img width="1248" height="350" alt="image" src="https://github.com/user-attachments/assets/40623696-922c-4025-a16e-dc6a3c1f7b1e" />
<img width="1115" height="535" alt="image" src="https://github.com/user-attachments/assets/57055a97-4e4f-4543-af60-b5e43a633af9" />


