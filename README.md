# Lab-2-CS2302
    def __init__(self, password, count, next):
        self.password = password
        self.count = count
        self.next = next


def read_it():
    x = None
    ps = open('3-thousand-combos.txt')
    line = ps.readline()
    while line:
        cur = x
        if cur is None:
            cur = Node(line.split(), 1, cur)
            print(cur.password)
        while cur is not None:
            if cur.password == line.split():
                cur.count += 1
                break
            cur = cur.next
    ps.close()


read_it()
