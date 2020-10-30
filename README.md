def extractGrade(x):
    x = x.split('-')
    y = float(x[1].strip('%'))
    return y

def classAverage(final_marks):
    total = 0
    num = int(len(final_marks))
    for i in range(num):
        total += extractGrade(final_marks[i])
    avg = total/num
    return avg

def classStdDev(final_marks):
    total = 0
    num = int(len(final_marks))
    for i in range(num):
        total += (extractGrade(final_marks[i])-classAverage(final_marks))**2
    std_dev = (total/num)**0.5
    return std_dev
   
