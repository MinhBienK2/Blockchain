# 1. Trình bày về hashing function và SHA-256

> ## Hashing function

-   Hashing function (hàm băm) là một phương pháp mã hóa dữ liệu để tạo ra một chuỗi đại diện ngắn gọn của dữ liệu đầu vào, gọi là giá trị băm (hash value). Trong blockchain, hàm băm được sử dụng để tạo ra mã xác thực cho các khối dữ liệu trong chuỗi khối.

<br>

> ## SHA-256

-   SHA-256 là một phương pháp mã hóa dữ liệu để tạo ra một chuỗi đại diện ngắn gọn của dữ liệu đầu vào, gọi là giá trị băm (hash value). Trong blockchain, hàm băm được sử dụng để tạo ra mã xác thực cho các khối dữ liệu trong chuỗi khối.

<br>

# 2. Trình bày về mã hóa đối xứng (symmetric cryptography) và mã hóa bất đối xứng (asymmetric cryptography)

Trong blockchain, mã hóa đối xứng **(symmetric cryptography)** và mã hóa bất đối xứng **(asymmetric cryptography)** được sử dụng để bảo vệ tính toàn vẹn và bảo mật dữ liệu.

> ## Mã hóa đối xứng (symmetric cryptography)

-   Mã hóa đối xứng (symmetric cryptography) được sử dụng trong blockchain để bảo mật dữ liệu trong các giao dịch. Trong blockchain, các giao dịch được mã hóa bằng cách sử dụng một khóa bí mật chung giữa người gửi và người nhận để đảm bảo tính toàn vẹn và bảo mật của dữ liệu.
-   Một số thuật toán mã hóa đối xứng phổ biến được sử dụng trong blockchain bao gồm AES (Advanced Encryption Standard) và DES (Data Encryption Standard). AES là một thuật toán mã hóa đối xứng phổ biến nhất được sử dụng trong blockchain để mã hóa dữ liệu trong các giao dịch.
-   Tuy nhiên, trong blockchain, mã hóa đối xứng thường không được sử dụng để mã hóa toàn bộ dữ liệu trong một khối vì điều đó có thể gây tốn nhiều tài nguyên tính toán. Thay vào đó, hàm băm (hashing function) được sử dụng để tạo ra một giá trị băm duy nhất cho mỗi khối, và giá trị băm này được sử dụng để kiểm tra tính toàn vẹn của khối trong quá trình đồng bộ hóa chuỗi khối.
-   chỉ được sử dụng cho các phần nhạy cảm của dữ liệu, như khóa riêng tư (private key) trong các giao dịch. Khi người dùng tạo một giao dịch, khóa riêng tư của họ sẽ được mã hóa bằng mã hóa đối xứng và gửi đến mạng blockchain để xác nhận giao dịch. Khi giao dịch được xác nhận, khóa riêng tư sẽ được giải mã và sử dụng để xác thực chữ ký điện tử (digital signature) của người gửi giao dịch.

###### Symmetric Cryptography

</div>
<br>

> ## Mã hóa bất đối xứng (asymmetric cryptography)

-   Mã hóa bất đối xứng là một hệ thống mã hóa sử dụng hai khóa khác nhau: khóa bí mật (private key) và khóa công khai (public key). Khóa bí mật được giữ bí mật và chỉ được sử dụng để giải mã thông tin, trong khi khóa công khai được chia sẻ công khai và được sử dụng để mã hóa thông tin. Mã hóa bất đối xứng đảm bảo tính toàn vẹn của các giao dịch trong blockchain và giúp người dùng xác thực danh tính của nhau một cách an toàn và bảo mật.
-   Trong blockchain, mã hóa bất đối xứng được sử dụng để xác thực người dùng và đảm bảo tính toàn vẹn của các giao dịch. Khi một người dùng tạo ra một giao dịch mới trên blockchain, họ sẽ tạo chữ ký số (digital signature) bằng cách sử dụng khóa bí mật của mình. Chữ ký số này sẽ được gắn vào giao dịch và chuyển đi trên mạng blockchain cùng với thông tin giao dịch.
-   Khi một nút trên mạng blockchain nhận được một giao dịch mới, nó sẽ sử dụng khóa công khai tương ứng với người dùng để giải mã chữ ký số. Nếu chữ ký số hợp lệ, tức là được tạo ra bởi người dùng đó sử dụng khóa bí mật của họ, thì giao dịch sẽ được xác thực và được thêm vào blockchain.

###### Asymmetric Cryptography

</div>

# 3. Trình bày cấu trúc chung của một block

###### Blockchain Structure

</div>
<br>

> ## Block Size

-   BlockSize (kích thước khối) là một trong những thông số quan trọng trong mạng blockchain, đó là kích thước tối đa cho mỗi block trong chuỗi blockchain. BlockSize được định nghĩa bằng số byte hoặc kilobyte (KB) và thường được thiết lập bởi những người điều hành mạng blockchain.
-   BlockSize ảnh hưởng trực tiếp đến khả năng xử lý và thời gian xác nhận của giao dịch trong mạng blockchain. Với BlockSize nhỏ, mạng blockchain có thể xử lý ít giao dịch hơn một lúc, nhưng việc xác nhận các giao dịch này sẽ nhanh hơn. Tuy nhiên, với BlockSize lớn, mạng blockchain có thể xử lý nhiều giao dịch hơn một lúc, nhưng thời gian xác nhận các giao dịch có thể chậm hơn do thời gian cần thiết để khai thác và xác minh các khối lớn hơn.
-   Ngoài ra, BlockSize cũng ảnh hưởng đến chi phí của giao dịch trong mạng blockchain. Khi BlockSize nhỏ, các giao dịch có thể phải đợi cho đến khi có đủ dung lượng trống trong khối mới để được xử lý, và những giao dịch có phí thấp hơn có thể bị bỏ qua hoặc chậm xử lý. Tuy nhiên, với BlockSize lớn, các giao dịch có thể được xử lý nhanh hơn, nhưng cũng có thể yêu cầu phí giao dịch cao hơn để được đưa vào khối.
-   BlockSize thường được điều chỉnh để cân bằng giữa hiệu suất mạng blockchain và tính khả dụng của nó. Các mạng blockchain khác nhau có các kích thước khối khác nhau, ví dụ như Bitcoin có BlockSize tối đa là 1 MB, Ethereum có BlockSize tối đa là 15 KB.

> ## Block Header

-   Block Header là một phần quan trọng trong cấu trúc của mỗi khối trong blockchain. Nó chứa các thông tin mô tả về khối, bao gồm các thông tin về khối trước đó trong chuỗi khối, phiên bản phần mềm sử dụng, thời gian tạo khối, độ khó của khối, nội dung giao dịch, giá trị băm của khối và nhiều thông tin khác.
    -   Phiên bản (Version): xác định phiên bản của phần mềm sử dụng để tạo khối.
    -   Giá trị băm khối trước đó (Previous Block Hash): xác định giá trị băm của khối trước đó trong chuỗi khối.
    -   Giá trị băm của các giao dịch (Merkle Root Hash): xác định giá trị băm của tất cả các giao dịch có trong khối.
    -   Thời gian tạo khối (Timestamp): xác định thời gian tạo khối.
    -   Độ khó (Difficulty): xác định mức độ khó để tìm được giá trị băm của khối.
    -   Giá trị nonce: giá trị này được tìm thấy bằng cách thử nghiệm các giá trị khác nhau để tạo ra giá trị băm đúng với độ khó đã cho.
    -   Giá trị băm của khối (Block Hash): xác định giá trị băm của toàn bộ khối.
-   Các thông tin trong Block Header được sử dụng để tạo ra giá trị băm của khối, được sử dụng để xác nhận tính toàn vẹn của khối trong quá trình đồng bộ hóa chuỗi khối. Mỗi khối trong chuỗi khối sẽ được liên kết với khối trước đó thông qua giá trị băm của khối trước đó trong trường Previous Block Hash của Block Header, tạo thành một chuỗi khối ngang hàng (blockchain) không thể thay đổi được mà bất kỳ ai cũng có thể xem xét được lịch sử các giao dịch trên blockchain.

> ## Transaction Counter

-   Trong mạng lưới blockchain, mỗi khối (block) bao gồm nhiều giao dịch (transaction) được thực hiện bởi các người dùng trên mạng. Transaction counter là một trường chỉ ra số lượng giao dịch có trong khối đó. Trường này là một số nguyên không dấu 32-bit và được mã hóa dưới dạng Little-endian.
-   Việc theo dõi transaction counter trong các khối là quan trọng để giám sát tốc độ xử lý và đảm bảo tính nhất quán của dữ liệu trên mạng lưới blockchain. Nếu số lượng giao dịch trong khối quá lớn, việc xử lý và truyền tải khối đó sẽ mất nhiều thời gian và tài nguyên hơn. Tuy nhiên, nếu số lượng giao dịch trong khối quá ít, thì việc sử dụng tài nguyên để tạo khối sẽ không được tối ưu.

> ## Transaction Data

-   Transaction data là trường của khối (block) chứa thông tin dữ liệu (data) về các giao dịch (transation) được thực hiện trong chuỗi blockchain. Mỗi giao dịch trong mạng blockchain sẽ được đóng gói vào một khối và có thể bao gồm thông tin về:
    -   Input: là thông tin về địa chỉ và số tiền Bitcoin được chuyển đi từ các giao dịch trước đó. Mỗi giao dịch mới sẽ sử dụng các đầu vào này để xác định số tiền Bitcoin có sẵn để chuyển đi.
    -   Output: là thông tin về địa chỉ và số tiền Bitcoin được chuyển đến trong giao dịch hiện tại. Mỗi giao dịch mới sẽ tạo ra các đầu ra mới này để chuyển tiền đến các địa chỉ tương ứng.
    -   ScriptSig: là mã ký hiệu được sử dụng để xác minh chữ ký số của người gửi giao dịch, đảm bảo rằng người gửi thực sự là chủ sở hữu của tiền.
    -   ScriptPubKey: là mã ký hiệu được sử dụng để xác định địa chỉ Bitcoin của người nhận tiền trong giao dịch.
    -   Locktime: là thời gian khoá (lock time) của giao dịch, có thể được sử dụng để xác định thời điểm nào mà giao dịch có thể được thực hiện hoặc không thể bị hoàn lại.
-   Tất cả các thành phần trên được mã hóa và kết hợp để tạo thành một đoạn mã hexa, gọi là transaction data (dữ liệu giao dịch), được lưu trữ trên mạng lưới blockchain. Các nút trên mạng lưới sẽ sử dụng transaction data này để xác định tính hợp lệ của mỗi giao dịch.

---
