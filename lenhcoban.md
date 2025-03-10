2. Git version:

   ` $ git --v`
   
   `git remote show origin`

    Kiểm tra phiên bản của Git.

3. Git config:

        $ git config --g user.name "Dev name"

        $ git config --g user.email "Dev email"

        $ git config --list

    Định cấu hình các biến cấu hình chung – Nếu bạn đang làm việc với các developer khác, bạn sẽ cần biết ai đang kiểm tra mã xuất nhập và thực hiện thay đổi.

4. Git help:

    Nếu bạn cần hỗ trợ, hãy sử dụng các lệnh:

        $ git help -a or $ git help --all - Hướng dẫn bạn có thể làm được những gì, tất cả các lệnh có thể.

        $ git config --help or $ git help config - Đưa bạn tới trang hướng dẫn chính thống của Git.

        $ git command -help - Xem tất cả các tùy chọn có sẵn cho lệnh cụ thể

5. Git mkdir:

        $ git mkdir folder_name - Tạo repository trong hệ thống local.

        $ cd folder_name - Di chuyển đến folder_name repository vừa tạo ra.

6. Git remote:

        $ git remote add origin https... <url> - Liên kết đến remote repository (local & GitHub)

        $ git remote set-url <name> <new url> - Thay đổi địa chỉ của remote repository đã Liên kết vào địa chỉ của <new url>.

        $ git remote rename <old> <new> - Thay đổi tên của remote repository đã Liên kết.

7. Git init:

        $ git init (Khởi tạo git trong thư mục dự án của bạn)

    Lệnh này được dùng khi bạn muốn tạo một phiên bản git mới cho một dự án.
8. Git status:

        $ git status

        $ git status --short

    (Kiểm tra trạng thái của kho lưu trữ)

    Giải thích:

    ?? - Tập tin không bị theo dõi

        A - Tệp được thêm vào giai đoạn

        M - Tệp đã sửa đổi

        D - Các tệp đã xóa

    Câu lệnh Git status dùng để kiểm tra status của repository.

9. Git add:

        $ git add . (Chú ý dấu chấm)

    Hoặc:

        $ git add --all (git add -A)

        $ git add index.html (có thể chỉ định trực tiếp tên tệp cần add)

    Add những thay đổi (bạn đã tạo mới hoặc chỉnh sửa) để thực hiện commit.

10. Git commit

        $ git commit -m "Thông điệp của bạn"

    Git commit: Ghi lại các thay đổi vào kho lưu trữ. (Cần thêm các thông điệp rõ ràng vào mỗi mục commit)

    Cách đặt tên branch hay commit nên rõ ràng, thể hiện branch đó, commit đó thực hiện feature gì hay là fix bug gì... (thường thì sẽ theo quy định của công ty)

11. Git diff:

        $ git diff So sánh sự khác biệt kể từ lần commit cuối cùng của bạn.

        $ git log Xem lịch sử làm việc với git (lịch sử commit)

12. Git push:

        $ git push -u origin branch_name - Push (đẩy) branch vào remote repository.

        $ git push - Push (đẩy) tất cả mọi thay đổi (đã commit) lên remote repository.

        $ git push -d origin branch_name - Xóa một branch trên remote repository.

        $ git push -f origin branch_name - Push force sẽ apply toàn bộ log ở local của bạn lên branch ở repo, bất chấp log 2 nơi khác nhau. (Xóa vĩnh viễn branch cũ Push branch mới. Dễ gây conflict cho người khác cẩn trọng trước khi dùng)

13. Git branch:

        $ git branch -M branch_name (main) - Đổi tên nhánh chính.

        $ git branch - Kiểm tra các nhánh hiện có của bạn ở local.

        $ git branch -c branch_name Hoặc: $ git checkout -b branch_name (Tạo và chuyển luôn sang nhánh mới) - Tạo một nhánh có tên “branch_name” và hợp nhất (merge) nó với nhánh chính.

        $ git branch -d branch_name - Xóa một nhánh tại local có tên: "branch_name" (branch đã được hợp nhất (push) vào remote repository)

        $ git branch -D branch_name - Xóa một nhánh tại local có tên: "branch_name" (branch đã commit nhưng chưa hợp nhất vào remote repository)

        $ git branch -a - Kiểm tra các branch hiện có trên remote repo của bạn.

14. Git checkout:

        $ git checkout -b branch_name (Tạo và chuyển luôn sang nhánh mới)

        $ git checkout branch_name - Lệnh trên giúp di chuyển không gian làm việc, kiểm tra tệp giữa các branch_name.

15. Git fetch: (Lấy code về nhưng chưa muốn merge)

        $ git fetch origin

    Git fetch cho phép CẬP NHẬT để xem điều gì đã thay đổi trên GitHub của bạn.

    Lệnh fetch (xác nhận nội dung thay đổi trong branch của remote repository) nhưng nội dung branch của local repository không bị thay đổi.

16. Git merge: (merge kết hợp nhánh hiện tại, với một nhánh được chỉ định.)

    Di chuyển về branch cần hợp nhất bằng lệnh checkout.

        $ git checkout branch_name1 (Nhánh nhận hợp nhất or nhánh hiện tại)

    Tiến hành hợp nhất:

        $ git merge branch_name2 (Nhánh chỉ định hợp nhất)

    (Nhánh hiện tại là nhánh bạn đang đứng, nhánh chỉ định là nhánh sau lệnh $ git merge)

    Lệnh trên giúp hợp nhất các branch (Hợp nhất branch_name2 vào branch_name1). (Chú ý xử lý xung đột code)

17. Git pull: (Hợp nhất từ xa)

        $ git pull origin main - Git pull kéo tất cả các thay đổi từ main về local.

        $ git pull - Git pull kéo tất cả các thay đổi từ branch_name về local.

        $ git pull origin - Git pull kéo tất cả các thay đổi từ kho lưu trữ từ xa vào branch bạn đang làm việc. (pull là sự kết hợp của 2 lệnh khác nhau: fetch và merge)

        $ git pull --rebase (Cach pull chống xung đột)

18. Git clone:

        $ git clone <url> (Địa chỉ dự án bạn muốn Clone) - Clone dự án có sẵn trên GitHub.

        $ git clone <url> folder_name - Clone đồng thời đổi tên dự án theo ý bạn khi save vào local.

19. Git stash:

        $ git stash save # Hoặc $ git stash - Lưu lại công việc đang làm ở branch này để chuyển sang branch khác (Khi bạn chưa muốn commit code)

        $ git stash list - Xem lại lịch sử thay đổi.

        $ git stash show stash@{n} - Xem lại lịch sử thay đổi cụ thể của lần stash save{n}.

        $ git stash apply stash@{1} - Apply thay đổi của lần stash save{n}.

        $ git stash clear - Xoá toàn bộ stash.

20. Git rebase: (Hợp nhất code)

    Di chuyển về nhánh nhận sự hợp nhất.

   ` $ git checkout branch_name1`

    Tiến hành hợp nhất.

    $ git rebase branch_name2 (Code từ branch_name2 được hợp nhất vào branch_name1)

    Tương đồng với merge nhưng có sự khác biệt như sau:

    Merge: Chỉ lấy nội dung commit cuối cùng của hai nhánh, tích hợp tạo thành commit mới. Các commit trước đó được giữ nguyên không thay đổi.

    Rebase: Lấy code từ branch_name2, từ những commit ở branch_name2 tích hợp đồng thời tái tạo lại commit mới ở branch_name1 (Các commit đã tồn tại bị bỏ đi).

21. Git revert:

`$ git revert <commit_id>`

Lệnh này tạo commit đảo ngược commit có commit_id được chọn.

`$ git reset –hard <commit_id>`

Lệnh này xoá toàn bộ các commit trước đó, đưa branch về trạng thái của commit_id được chọn.

`$ git reset –soft <commit_id>` 

Đưa branch về trạng thái của commit_id được chọn. Giữ nguyên tất cả thay đổi của file và các thay đổi ở stage. (Được khuyến khích sử dụng)