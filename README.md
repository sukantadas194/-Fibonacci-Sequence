# -Fibonacci-Sequence


def fib(n):
    N = input("Enter no. : ")       #User Input

    try:
        n = int(N)                  #Converting stirng value into integer
        a = 0                       #'a' & 'b' values are fixed for Fibonacci series
        b = 1

        if n == 1:
            print(a)                #if input is '1' output will be '0'
            return

        if n == 0:
            print("Enter input correctly")
            print("Number must be a positive value & greater than '0'")
            print("Start over again..")
            fib(n)

        if n >= 2:
            print("Do you want", n, "Fibonacci numbers?")
            A = input("Ans : ")
            print(A)

        if A == "yes" or A == "YES" or A == "Yes":
            print("Sl no.", "|", "Fibonacci Sequence")
            print(" ", a, '.', "         ", "0")
            print(" ", b, '.', "         ", "1")
            for i in range(2, n):                              #creating 1st conditional sequence
                c = a + b
                a = b
                b = c
                print(" ", i, '.', "         ", c)
            return

        if A == "no" or A == "NO" or A == "No":
            print("Do you want Fibonacci numbers upto", n, "?")
            B = input("Ans : ")
            print(B)

        else:
            print("Answer it by typing 'Yes' or 'No' only")
            print("Start again..👇")
            fib(n)

        if B == "yes" or B == "YES" or B == "Yes":
            print("Sl no.", "|", "Fibonacci Sequence")
            print(" ", a, '.', "         ", "0")
            print(" ", b, '.', "         ", "1")
            for i in range(2, n):                             #creating 2nd conditional sequence
                c = a + b
                a = b
                b = c
                if c <= n:
                    print(" ", i, '.', "         ", c)
            return

        if B == "no" or B == "NO" or B == "No":
            try:
                print("Start again..")
            except:
                print("Start again..")

        else:
            print("Answer it by typing only 'Yes' or 'No'")
            print("Start again..👇")
            fib(n)


    except:
        print("Answer it by typing only 'Yes' or 'No'")
        print("Start over again..")
        fib(n)

fib(print("Let's Start.."))
