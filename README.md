Problem: Remove Nth Node From End of List

Problem Description:
Given the head of a singly linked list, remove the nth node from the end of the list and return its head.

Approach:
-We solve this problem using the "two-pointer technique", allowing us to achieve the solution in one pass (a single traversal of the list).

Dummy Node: To handle edge cases (like deleting the head of the list), we use a dummy node that points to the head of the list. This helps us easily handle situations where the head node needs to be deleted.

Fast and Slow Pointers: We use two pointers (fast and slow) that start at the dummy node.

Step-by-Step Solution:
Move the fast pointer n+1 steps ahead:
We move the fast pointer n+1 steps ahead in the list. This creates a gap of n nodes between the fast and slow pointers, allowing us to determine which node is n steps from the end.

Move both fast and slow pointers together:
We move both fast and slow pointers one step at a time until the fast pointer reaches the end of the list. At this point, the slow pointer will be just before the node we want to delete.

Delete the node:
We adjust the next pointer of the slow pointer to skip over the node to be deleted. We then delete the node from memory.

Time and Space Complexity:
Time Complexity: O(sz), where sz is the number of nodes in the list. Since we only make one pass through the list, the time complexity is linear.

Space Complexity: O(1), as we use a constant amount of space (just pointers) and don't require extra data structures.

Examples:

Example 1:
Input:  head = [1, 2, 3, 4, 5], n = 2
Output: [1, 2, 3, 5]
In this case, the 2nd node from the end, which is 4, is removed.

Example 2:
Input:  head = [1], n = 1
Output: []
Here, the only node in the list is removed, leaving an empty list.



###########################################################################################



Problem: Remove Nth Node From End of List

Problemin Tanımı:
Verilen bir bağlı listenin başından (head) başlayarak, sondan n. elemanı silin ve kalan listenin başını döndürün.

Yaklaşım:
Bu soruyu "iki işaretçi tekniği" (two-pointer technique) kullanarak, tek geçişte (one pass) çözmeyi amaçlıyoruz.

Dummy Node Kullanımı: Bağlı listenin başını silme gibi edge (sınır) durumları yönetebilmek için bir "dummy node" ekliyoruz. Bu düğüm başa bağlanır ve silinecek olan düğümün öncesine ulaşmamızı sağlar.

Fast ve Slow Pointers: İki işaretçi (fast ve slow) kullanıyoruz. Her ikisi de başlangıçta dummy düğümüne işaret eder.

Adım Adım Çözüm:
Fast işaretçisini n+1 adım ilerletin:
fast işaretçisini, silmek istediğimiz düğümün öncesine ulaşacak şekilde, baştan n+1 adım ilerletiyoruz. Bu, fast ve slow işaretçileri arasında n adımlık bir mesafe oluşturur.

Fast ve Slow işaretçilerini birlikte hareket ettirin:
fast işaretçisi sona ulaşana kadar, fast ve slow işaretçilerini aynı anda birer adım ileriye taşıyoruz. Bu sayede, slow işaretçisi silmek istediğimiz düğümün bir öncesine ulaşır.

Silme işlemi:
slow işaretçisinin next pointer'ı, silmek istediğimiz düğümün sonrasına yönlendirilir. Ardından silinen düğüm bellekten temizlenir.

Zaman ve Alan Karmaşıklığı:
Zaman karmaşıklığı: O(sz), burada sz listenin eleman sayısıdır. Çünkü yalnızca bir geçiş yapıyoruz ve her adımda sadece sabit işlemler gerçekleştiriyoruz.

Alan karmaşıklığı: O(1), ek bir veri yapısı kullanılmadığı için sabit alan kullanımı vardır.

Örnek 1:
Input:  head = [1, 2, 3, 4, 5], n = 2
Output: [1, 2, 3, 5]
Burada sondan 2. eleman, yani 4 siliniyor.

Örnek 2:
Input:  head = [1, 2], n = 1
Output: [1]
Burada sondan 1. eleman, yani 2 siliniyor ve liste sadece 1 elemanından oluşuyor.



